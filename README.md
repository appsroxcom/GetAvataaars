# GetAvataaars
Easily add avatar picker dialog in your Android application.

<img src="art/screenshot1.png" width=200/>

## Setup
In project-level build.gradle:
```
maven { url 'https://jitpack.io' }
```

In app-level build.gradle:
```
implementation 'com.github.appsroxcom:GetAvataaars:v1.1.0'
```

## Usage

To show avatar picker dialog -

```
        AvatarDialog avatarDialog = AvatarDialog.newInstance(avatarUri);
        avatarDialog.show(getSupportFragmentManager(), "dialog_avatar");
```

To get avatar bitmap -

```
public class MainActivity extends AppCompatActivity implements AvatarDialog.AvatarDialogListener {

    private String avatarUri = null;

    @Override
    public void onAvatarUpdate(String avatarUri, Bitmap avatarBitmap) {
        this.avatarUri = avatarUri;
    }
}
```
