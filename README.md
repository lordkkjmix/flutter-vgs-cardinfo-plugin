# VGS Card Info

Flutter plugin to display VGS Card info using TextView or View

## Installation
Add the dependency in your pubspec.yaml 

```yaml
vgscardinfo:
    git:
      url: git://github.com/djamoapp/flutter-vgs-cardinfo-plugin.git
```

## Widgets Usage
### VgsTextView 
This widget displays only one VGS card data using the token.
```dart
VgsTextView(
  key: Key("<token_key>"),
  id: "<token_key>",
  token: "<pan_token>",
  vaultId: VAULT_ID, // Refers to a constant declaration
  path: DJAMO_VGS_PATH, // Refers to a constant declaration
))
```
This widget comes with the **copyContent** method that copy the content of a VgsTextView rendered
```dart
VgsTextView.copyContent(id: "<token_key>");

```

### VgscardInfoView
This widget displays all VGS card data in one view
```dart
VgsCardInfoConfig _vgsCardInfoConfig = VgsCardInfoConfig(
    cvvToken: "<cvvToken>",
    expiryDateToken: "<expiryDateToken>",
    nameToken: "<nameToken>",
    panToken: "<panToken>",
    vgsPath: DJAMO_VGS_PATH, // Refers to a constant declaration
    vgsVaultId: VAULT_ID, // Refers to a constant declaration
  );
  
VgscardInfoView(
  vgsCardInfoConfig: _vgsCardInfoConfig,
),
```
## Support
This project is a starting point for a Flutter
[plug-in package](https://flutter.dev/developing-packages/),
a specialized package that includes platform-specific implementation code for
Android and/or iOS.

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

