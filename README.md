# QtCreator theme with a contrasted scrollbar
How to make QtCreator's scrollbar contrasted, and a drop in theme that is 'Flat Dark' with the contrasted scroll bar

### Edit your own preferred theme
The only modification is setting `PreferredStyles` to `Windows` in the appropriate `.creatortheme` file. Otherwise, the color for the scrollbar is too close to its background and it's a daily annoyance. Note this modification will make QtCreator look a bit less modern in its UI

To install my [flat-dark-contrasted.creatortheme](https://raw.githubusercontent.com/Kidev/QtCreator-scrollbar-contrasted-theme/refs/heads/main/flat-dark-contrasted.creatortheme), download said file and add it to the folder `$QT_ROOT/Tools/QtCreator/share/qtcreator/themes`
Then change the theme in Qt Creator, the menu is in `Edit > Preferences > Environment > Theme`
![image](https://github.com/user-attachments/assets/b52b62f4-c7aa-404a-a945-ef5d186a8289)

To make your own, copy an existing theme from within the folder `$QT_ROOT/Tools/QtCreator/share/qtcreator/themes`.
Rename the file, and make those changes:
```diff
--- a/theme.creatortheme
+++ b/theme.creatortheme
@@ -1,8 +1,8 @@
 [General]
 Includes=dark.figmatokens
-ThemeName=$OLD_THEME_NAME
-PreferredStyles=
+ThemeName=$CONTRASTED_THEME_NAME
+PreferredStyles=Windows
```
Don't forget to also change `ThemeName` to change its display name in Qt Creator.
