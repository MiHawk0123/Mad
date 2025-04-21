#6( Linear Layout with Name, Age, Mobile)
XML (activity_main.xml):

------------------------

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout

 xmlns:android="http://schemas.android.com/apk/res/android"

 android:orientation="vertical"

 android:layout_width="match_parent"

 android:layout_height="match_parent"

 android:padding="16dp">

 <EditText

 android:id="@+id/editTextName"

 android:layout_width="match_parent"

 android:layout_height="wrap_content"

 android:hint="Name" />

 <EditText

 android:id="@+id/editTextAge"

 android:layout_width="match_parent"

 android:layout_height="wrap_content"

 android:hint="Age"

 android:inputType="number" />

 <EditText

 android:id="@+id/editTextMobile"

 android:layout_width="match_parent"

 android:layout_height="wrap_content"

 android:hint="Mobile Number"

 android:inputType="phone" />

 <Button

 android:id="@+id/buttonSubmit"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:text="Submit" />

</LinearLayout>
 package com.example.myapplication;

import android.os.Bundle;

import android.widget.Button;

import android.widget.EditText;

import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

 EditText editTextName, editTextAge, editTextMobile;

 Button buttonSubmit;

 @Override

 protected void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);

 setContentView(R.layout.activity_main);

 // Initialize views

 editTextName = findViewById(R.id.editTextName);

 editTextAge = findViewById(R.id.editTextAge);

 editTextMobile = findViewById(R.id.editTextMobile);

 buttonSubmit = findViewById(R.id.buttonSubmit);

 // Set button click listener

 buttonSubmit.setOnClickListener(v -> {

 String name = editTextName.getText().toString();

 String age = editTextAge.getText().toString();

 String mobile = editTextMobile.getText().toString();

 // Display the input using a Toast

 Toast.makeText(MainActivity.this,

 "Name: " + name + "\nAge: " + age + "\nMobile: " + mobile,

 Toast.LENGTH_LONG).show();

 });

 }

}
