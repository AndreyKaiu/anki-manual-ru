# Anki не подхватывает тему GTK на Gnome/Linux

Вы можете обойти эту проблему, явно указав Anki, какая используется тема GTK. Выполните следующие команды в терминале:

```shell
theme=$(gsettings get org.gnome.desktop.interface gtk-theme)
echo "gtk-theme-name=$theme" >> ~/.gtkrc-2.0
echo "export GTK2_RC_FILES=$HOME/.gtkrc-2.0" >> ~/.profile
```

Затем выйдите из системы и войдите снова в ваш компьютер, и Anki должна подхватить тему GTK.
