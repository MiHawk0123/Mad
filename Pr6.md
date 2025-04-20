#6
MainActivity.java

import android.os.Bundle;

import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

private TextView nameTextView, ageTextView, mobileNumberTextView;

@Override

protected void onCreate(Bundle savedInstanceState) {

super.onCreate(savedInstanceState);

setContentView(R.layout.activity_main);

nameTextView = findViewById(R.id.name_text_view);

ageTextView = findViewById(R.id.age_text_view);

mobileNumberTextView = findViewById(R.id.mobile_number_text_view);

nameTextView.setText("Name: John Doe");

ageTextView.setText("Age: 25");

mobileNumberTextView.setText("Mobile Number: 1234567890");

}

}
activity_main.xml

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"

android:layout_width="match_parent"

android:layout_height="match_parent"

android:orientation="vertical">

<TextView

android:id="@+id/name_text_view"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:textSize="24sp" />

<TextView

android:id="@+id/age_text_view"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:textSize="24sp" />

<TextView

android:id="@+id/mobile_number_text_view"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:textSize="24sp" />

</LinearLayout>
