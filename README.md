# Custom template for Gitea 1.9.6
Add `VS` button to repository home page, this new button allows to clone the repository to VSCODE directly.

## Windows browser configuring
How to configure the browser so that it does not request to open vscode every time we use the button

### Chrome
Chrome will ask *"Open Visual Studio Code?"*, if the check *"Always open these types of links in the associated app"* is not visible you can create or edit the registry subkey `ExternalProtocolDialogShowAlwaysOpenCheckbox` with value 1

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Google\Chrome]
"ExternalProtocolDialogShowAlwaysOpenCheckbox"=dword:00000001
```
### Edge
Edit or create the registry key `vscode` and put the value of subkey `WarnOnOpen` to 1
```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Internet Explorer\ProtocolExecute\vscode]
"WarnOnOpen"=dword:00000001
```
### Firefox
the browser asks which application opens the link and allows you to remember the selection