# Ex_8_CheckBox
Develop a program to create a option menu using checkboxes and display the toast selected checkboxes with Android Studio
## AIM:
To Develop a program for creating a option menu using checkboxes and display the toast selected checkboxes with Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Once the Selected check box displayed to the user processed in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
/*
Program to create an Option Menu
Developed by:LOGESHWARI.P
RegisterNumber:212221230055  
*/
```

## MainActivity.java:
```
package com.example.ex_8;

import androidx.appcompat.app.AppCompatActivity;
import android.view.View;
import android.widget.CheckBox;
import android.widget.Toast;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
    private CheckBox chkAndroid, chkJava, chkPhp, chkCpp, chkC;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        chkAndroid = findViewById(R.id.chkAndroid);
        chkJava = findViewById(R.id.chkJava);
        chkPhp = findViewById(R.id.chkPhp);
        chkCpp = findViewById(R.id.chkCpp);
        chkC = findViewById(R.id.chkC);
    }
    public void showSelected(View view) {

        String selected = "You selected: \n";

        if(chkAndroid.isChecked())
            selected += "Android";

        if(chkJava.isChecked())
            selected += "\nJava";

        if(chkPhp.isChecked())
            selected += "\nPHP";

        if(chkCpp.isChecked())
            selected += "\nCPP";

        if(chkC.isChecked())
            selected += "\nC";

        Toast.makeText(MainActivity.this, selected, Toast.LENGTH_SHORT).show();
    }
}
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:gravity="center"
        android:text="Select Your favourite Programming language"
        style="@style/TextAppearance.AppCompat.Large"
        android:layout_margin="10dp"
        android:textStyle="bold"/>

    <CheckBox
        android:id="@+id/chkAndroid"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Android"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkJava"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Java"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkPhp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="PHP"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkCpp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="CPP"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkC"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="C"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <Button android:id="@+id/btnDisplay"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Display"
        android:layout_marginTop="20dp"
        android:onClick="showSelected"/>

</LinearLayout>
```
## Output
![244950375-142b887b-c912-4dda-8f6b-b629586cbdb4](https://github.com/logeshwari2004/Ex_8_CheckBox/assets/94211349/b20e128e-34fd-4dbb-baf4-b1eb9777c0d7)

![244950400-aabe9506-57c5-41ac-aa9f-316b77c9c89f](https://github.com/logeshwari2004/Ex_8_CheckBox/assets/94211349/a2ebfa16-58ba-4fb9-8965-2b7823b71abc)


## Result:
Thus a Simple Android Application to create an check box and display the selected check box using Android Studio was developed and executed successfully.
