#pr 8
MainActivity.java

import android.os.Bundle;

import android.widget.DatePicker;

import android.widget.TimePicker;

import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

private DatePicker datePicker;

private TimePicker timePicker;

@Override

protected void onCreate(Bundle savedInstanceState) {

super.onCreate(savedInstanceState);

setContentView(R.layout.activity_main);

datePicker = findViewById(R.id.date_picker);

timePicker = findViewById(R.id.time_picker);

datePicker.init(2022, 0, 1, (view, year, month, day) -> {

Toast.makeText(MainActivity.this, "Selected Date: " + day + "/" + (month + 1) + "/" + year,

Toast.LENGTH_SHORT).show();

});

timePicker.setOnTimeChangedListener((view, hour, minute) -> {

Toast.makeText(MainActivity.this, "Selected Time: " + hour + ":" + minute,

Toast.LENGTH_SHORT).show();

});

}

}

activity_main.xml

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"

android:layout_width="match_parent"

android:layout_height="match_parent"

android:orientation="vertical">

<DatePicker

android:id="@+id/date_picker"

android:layout_width="match_parent"

android:layout_height="wrap_content" />
<TimePicker

android:id="@+id/time_picker"

android:layout_width="match_parent"

android:layout_height="wrap_content" />

</LinearLayout>
