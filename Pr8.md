#pr 8(Time Picker and Date Picker)
XML (activity_main.xml):

------------------------

<LinearLayout 

 xmlns:android="http://schemas.android.com/apk/res/android"

 android:orientation="vertical"

 android:layout_width="match_parent"
android:layout_height="match_parent"

 android:gravity="center"

 android:padding="16dp">

 <DatePicker android:id="@+id/datePicker" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:datePickerMode="spinner" />

 <Button android:id="@+id/btnDate" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:text="Set Date" />

 <TextView android:id="@+id/tvDate" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:textSize="18sp" android:textStyle="bold" />

 <TimePicker android:id="@+id/timePicker" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:timePickerMode="spinner" />

 <Button android:id="@+id/btnTime" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:text="Set Time" />

 <TextView android:id="@+id/tvTime" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:textSize="18sp" android:textStyle="bold" />

</LinearLayout>

Java (MainActivity.java):

-------------------------

package com.example.datetimepicker;

import android.os.Bundle;

import android.widget.*;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

 DatePicker datePicker;

 TimePicker timePicker;

 Button btnDate, btnTime;

 TextView tvDate, tvTime;

 @Override

 protected void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);

 setContentView(R.layout.activity_main);

 datePicker = findViewById(R.id.datePicker);

 timePicker = findViewById(R.id.timePicker);

 btnDate = findViewById(R.id.btnDate);

 btnTime = findViewById(R.id.btnTime);

 tvDate = findViewById(R.id.tvDate);

 tvTime = findViewById(R.id.tvTime);

 timePicker.setIs24HourView(true);

 btnDate.setOnClickListener(v -> {

 int day = datePicker.getDayOfMonth();

 int month = datePicker.getMonth() + 1;

 int year = datePicker.getYear();
 tvDate.setText("Date: " + day + "/" + month + "/" + year);

 });

 btnTime.setOnClickListener(v -> {

 int hour = timePicker.getHour();

 int minute = timePicker.getMinute();

 tvTime.setText("Time: " + hour + ":" + minute);

 });

 }

}
