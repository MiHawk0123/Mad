#pr 4
MainActivity.java

import android.os.Bundle;

import android.view.View;

import android.widget.ArrayAdapter;

import android.widget.AutoCompleteTextView;

import android.widget.Button;

import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

private AutoCompleteTextView searchEditText;

private Button searchButton;

@Override

protected void onCreate(Bundle savedInstanceState) {

super.onCreate(savedInstanceState);

setContentView(R.layout.activity_main);

searchEditText = findViewById(R.id.search_edit_text);

searchButton = findViewById(R.id.search_button);

String[] suggestions = {"Apple", "Banana", "Cherry", "Date", "Elderberry"};

ArrayAdapter<String> adapter = new ArrayAdapter<>(this,

android.R.layout.simple_dropdown_item_1line, suggestions);

searchEditText.setAdapter(adapter);

searchButton.setOnClickListener(new View.OnClickListener() {

@Override
public void onClick(View v) {

String searchQuery = searchEditText.getText().toString();

Toast.makeText(MainActivity.this, "Searching for: " + searchQuery,

Toast.LENGTH_SHORT).show();

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

<AutoCompleteTextView

android:id="@+id/search_edit_text"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:hint="Search" />

<Button

android:id="@+id/search_button"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:text="Search" />

</LinearLayout>
