# Mad
Pr1
MainActivity.java

import android.app.Activity;

import android.bluetooth.BluetoothAdapter;

import android.os.Bundle;

import android.view.View;

import android.widget.ToggleButton;

public class MainActivity extends Activity {

private BluetoothAdapter bluetoothAdapter;

private ToggleButton toggleButton;

@Override

protected void onCreate(Bundle savedInstanceState) {

super.onCreate(savedInstanceState);

setContentView(R.layout.activity_main);

bluetoothAdapter = BluetoothAdapter.getDefaultAdapter();

toggleButton = findViewById(R.id.toggle_button);

toggleButton.setOnCheckedChangeListener((buttonView, isChecked) -> {

if (isChecked) {

bluetoothAdapter.enable();

toggleButton.setText("Bluetooth is On");

} else {

bluetoothAdapter.disable();

toggleButton.setText("Bluetooth is Off");

}

});

}

}

activity_main.xml

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"

android:layout_width="match_parent"

android:layout_height="match_parent"

android:orientation="vertical">

<ToggleButton

android:id="@+id/toggle_button"

android:layout_width="wrap_content"

android:layout_height="wrap_content"
android:text="Bluetooth is Off"

android:textSize="24sp"

android:checked="false" />

</LinearLayout>
