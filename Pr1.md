#pr 1(toggle bluetooth)
XML (activity_main.xml):


<LinearLayout 

 xmlns:android="http://schemas.android.com/apk/res/android"

 android:orientation="vertical"

 android:layout_width="match_parent"

 android:layout_height="match_parent"

 android:gravity="center"

 android:padding="16dp">

 <ToggleButton

 android:id="@+id/toggleButton"

 android:layout_width="wrap_content"

 android:layout_height="wrap_content"

 android:textOn="Bluetooth ON"

 android:textOff="Bluetooth OFF"/>

</LinearLayout>

Java (MainActivity.java):

-------------------------

package com.example.bluetooth;

import android.bluetooth.BluetoothAdapter;

import android.os.Bundle;

import android.widget.ToggleButton;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

 ToggleButton toggleButton;

 BluetoothAdapter bluetoothAdapter;

 @Override

 protected void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);

 setContentView(R.layout.activity_main);

 toggleButton = findViewById(R.id.toggleButton);

 bluetoothAdapter = BluetoothAdapter.getDefaultAdapter();

 toggleButton.setOnCheckedChangeListener((buttonView, isChecked) -> {

 if (isChecked) bluetoothAdapter.enable();

 else bluetoothAdapter.disable();

 });

 }

