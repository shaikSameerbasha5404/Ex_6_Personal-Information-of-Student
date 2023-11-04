# Ex_6_Personal-Information-of-Student
Develop a program to accept personal information from the end user using Text View and Edit Text and display the information of the student.

## AIM:
To develop a program to accept personal information from the end user using Text View and Edit Text and display the information of the student using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Accept the Personal Information from the User and display the information given in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
/*
Program to develop personal information for student
Developed by: Shaik Sameer Basha 
RegisterNumber:  212222240093
*/
```

## MainActivity.java:
```
package com.example.smsintent;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;
import android.graphics.drawable.Drawable;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.LinearLayout;
import android.widget.Toast;

import java.util.Date;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText name,dob,mail,number;
        Button btn;
        name=findViewById(R.id.Name);
        dob=findViewById(R.id.dob);
        mail=findViewById(R.id.mail);
        number=findViewById(R.id.number);
        btn=findViewById(R.id.btn);
        LinearLayout lln=findViewById(R.id.lln);
        btn.setOnClickListener(new View.OnClickListener() {
            @SuppressLint("ResourceAsColor")
            @Override
            public void onClick(View view) {
                String n=name.getText().toString();
                String d =dob.getText().toString();
                String m=mail.getText().toString();
                String nu=number.getText().toString();
                if(n.isEmpty() || d.isEmpty() || m.isEmpty() || nu.isEmpty())
                {
                    Toast.makeText(MainActivity.this, "Please Enter Your Details", Toast.LENGTH_SHORT).show();
                    lln.setBackgroundColor(getResources().getColor(R.color.black));
                }
                else {
                    Toast.makeText(MainActivity.this, "Name :" + n + "DoB :" + d + "Mail :" + m + "Number :" + nu, Toast.LENGTH_LONG).show();
                    lln.setBackgroundColor(getResources().getColor(R.color.Green));

                }
            }
        });
    }
}
```

## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    tools:context=".MainActivity"
    android:id="@+id/lln">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Student Information "
        android:textSize="20dp"
        android:textStyle="bold"
        android:layout_marginBottom="20dp"
        android:textColor="@color/Red"/>
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="15"
        android:hint="Enter your Name"
        android:id="@+id/Name"
        android:inputType="textPersonName"
        android:textSize="20sp"
        android:textStyle="bold"
        android:layout_marginTop="20dp"/>
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="15"
        android:hint="Enter DOB"
        android:id="@+id/dob"
        android:inputType="date"
        android:textSize="20sp"
        android:textStyle="bold"
        android:layout_marginTop="20dp"/>
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="15"
        android:hint="Enter your Email"
        android:id="@+id/mail"
        android:inputType="textEmailAddress"
        android:textSize="20sp"
        android:textStyle="bold"
        android:layout_marginTop="20dp"/>
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="15"
        android:hint="Enter your contact Number"
        android:id="@+id/number"
        android:inputType="text"
        android:textSize="20sp"
        android:textStyle="bold"
        android:layout_marginTop="20dp"/>
    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="20dp"
        android:text="Submit"
        android:id="@+id/btn"/>



</LinearLayout>
```

## AndroidMainfest.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    package="com.example.smsintent">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.SMSIntent"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## Output:

![Screenshot (224)](https://github.com/shaikSameerbasha5404/Ex_6_Personal-Information-of-Student/assets/118707756/b8f79c6a-d116-420a-801c-84dd75be0b9a)


## Result:
Thus a Simple Android Application to create personal information from the end user and display the information of the student using Android Studio was developed and executed successfully.
