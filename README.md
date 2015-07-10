letterpress
==============
Custom fonts without writing code.

show image here.

Add custom fonts to your app with out writing code, just add the fonts to your them and use the customViews.

## Sample
Just define the views you want to apply the custom fonts on.

    <resources>
        <!-- Base application theme. -->
        <style name="BaseTheme" parent="Theme.AppCompat.Light.DarkActionBar">
            <!-- Customize your theme here. -->
            <item name="android:autoCompleteTextViewStyle">@style/FontAutoCompleteTextViewStyle</item>
            <item name="android:buttonStyle">@style/FontButtonStyle</item>
            <item name="android:checkboxStyle">@style/FontCheckBoxStyle</item>
            <item name="android:editTextStyle">@style/FontEditTextStyle</item>
            <item name="android:radioButtonStyle">@style/FontRadioButtonStyle</item>
            <item name="android:textViewStyle">@style/FontTextViewStyle</item>
            <item name="android:buttonStyleToggle">@style/FontToggleButton</item>
            <item name="autoCompleteTextViewStyle">@style/FontAutoCompleteTextViewStyle</item>
            <item name="buttonStyle">@style/FontButtonStyle</item>
            <item name="checkboxStyle">@style/FontCheckBoxStyle</item>
            <item name="editTextStyle">@style/FontEditTextStyle</item>
            <item name="radioButtonStyle">@style/FontRadioButtonStyle</item>
        </style>
        <style name="AppTheme" parent="BaseTheme">
        </style>
    </resources>

define the custom fonts that are in the assets folder, overriding the default parent style should make it uniform across the app. This is not required though.

    <resources>
        <style name="FontButtonStyle" parent="Widget.AppCompat.Button">
            <item name="pix_font">fonts/Action_Man.ttf</item>
            <item name="pix_fontBold">fonts/Action_Man_Bold.ttf</item>
            <item name="pix_fontItalic">fonts/Action_Man_Italic.ttf</item>
            <item name="pix_fontBoldItalic">fonts/Action_Man_Bold_Italic.ttf</item>
        </style>
        .....
        <style name="FontTextViewStyle" parent="@android:style/TextAppearance.Widget.TextView">
            <item name="pix_font">fonts/Action_Man.ttf</item>
            <item name="pix_fontBold">fonts/Action_Man_Bold.ttf</item>
            <item name="pix_fontItalic">fonts/Action_Man_Italic.ttf</item>
            <item name="pix_fontBoldItalic">fonts/Action_Man_Bold_Italic.ttf</item>
        </style>
    </resources>

Then in your layouts just use `FontTextView` instead of `TextView` and it will use the Action_Man font.
    <com.pixplicity.fontview.FontTextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="custom font from theme"/>

