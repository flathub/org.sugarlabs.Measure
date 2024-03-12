# Measure Activity Flatpak

To know more refer https://github.com/sugarlabs/Measure

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.Measure.git
cd org.sugarlabs.Measure
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.Measure.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Measure
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Measure.json
```