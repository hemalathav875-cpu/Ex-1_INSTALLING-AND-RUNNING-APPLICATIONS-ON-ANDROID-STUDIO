# Ex-1_INSTALLING-AND-RUNNING-APPLICATIONS-ON-ANDROID-STUDIO

# REGISTER NO:212225230099
# EX.NO:1
# AIM
To develop a simple Student Details Android application using Android Studio to enter and display student information.

# ALGORITHM
```
Open Android Studio and create a new project.

Design the user interface using XML.

Create input fields for student name, register number and department.

Add a Submit button.

Write Java code to get the entered details.

Display the student details when the Submit button is clicked.

```
# PROGRAM:

# MainActivity.java
```
package com.example.ex1app;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText name, regno, dept;
    Button submit;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        name = findViewById(R.id.name);
        regno = findViewById(R.id.regno);
        dept = findViewById(R.id.dept);
        submit = findViewById(R.id.submit);
        result = findViewById(R.id.result);

        submit.setOnClickListener(v -> {
            String n = name.getText().toString();
            String r = regno.getText().toString();
            String d = dept.getText().toString();

            result.setText(
                    "Student Name: " + n +
                            "\nRegister Number: " + r +
                            "\nDepartment: " + d
            );
        });
    }
}
```
# activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="25dp"
    android:gravity="center"
    android:background="#F4F5FB">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="STUDENT DETAILS"
        android:textSize="25sp"
        android:textStyle="bold"
        android:textColor="#6558D3"
        android:layout_marginBottom="30dp"/>

    <EditText
        android:id="@+id/name"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Student Name"/>

    <EditText
        android:id="@+id/regno"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Register Number"/>

    <EditText
        android:id="@+id/dept"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Department"/>

    <Button
        android:id="@+id/submit"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="SUBMIT"
        android:layout_marginTop="20dp"
        android:backgroundTint="#6558D3"/>

    <TextView
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="18sp"
        android:textColor="#222222"
        android:layout_marginTop="25dp"/>

</LinearLayout>
```

# OUTPUT:
<img width="297" height="666" alt="Screenshot 2026-11-06 090629" src="https://github.com/user-attachments/assets/b6bec6c6-c7ed-4208-b262-1e122deaeb2a" />


# RESULT

Thus, the Student Details Android application was successfully developed using Android Studio. The application accepts and displays student information successfully.
