#7
MainActivity.java

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.ProgressBar;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

private ProgressBar progressBar;

private Button startButton;

@Override

protected void onCreate(Bundle savedInstanceState) {

super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

progressBar = findViewById(R.id.progress_bar);

startButton = findViewById(R.id.start_button);

startButton.setOnClickListener(v -> {

progressBar.setVisibility(View.VISIBLE);

startButton.setEnabled(false);

// Simulate some work

new Thread(() -> {

try {

Thread.sleep(5000);

} catch (InterruptedException e) {

e.printStackTrace();

}

runOnUiThread(() -> {

progressBar.setVisibility(View.GONE);

startButton.setEnabled(true);

});

}).start();

});

}

}

activity_main.xml

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"

android:layout_width="match_parent"

android:layout_height="match_parent"

android:orientation="vertical">

<ProgressBar

android:id="@+id/progress_bar"

android:layout_width="wrap_content"

android:layout_height="wrap_content"

android:visibility="gone" />

<Button

android:id="@+id/start_button"

android:layout_width="wrap_content"

android:layout_height="wrap_content"

android:text="Start" />

</LinearLayout>
