# Universal Tool — releases

Signed `.zxp` builds of **Universal Tool**, a MoBar-style toolbar panel for After Effects (296 tools). The panel checks this repo for new versions.

## Install on a new PC

1. Download the latest **`UniversalTool-x.y.z.zxp`** from [Releases → Latest](https://github.com/dothack009/universal-tool-releases/releases/latest).
2. Install it with **[ZXP Installer](https://aescripts.com/learn/zxp-installer/)** (free, Mac & Windows). Drag the `.zxp` onto the app.
3. Restart After Effects, then open **Window → Extensions → Universal Tool**.

## Updates

The panel checks for new releases when it opens. When one is available, it shows **"Update x.y.z available → Install"**. Click Install, then restart After Effects. If Universal Tool was installed for all users, your computer asks for your admin password.

You can also check by hand in **≡ Settings → Updates → Check for updates**.

## If the panel opens blank

This is Adobe's [known ZXP signing issue](https://github.com/Adobe-CEP/CEP-Resources/blob/master/ZXPSignCMD/KnownIssue2024.md). Turn on CEP debug mode once, then restart After Effects:

- **Mac** (Terminal): `for v in 9 10 11 12 13; do defaults write com.adobe.CSXS.$v PlayerDebugMode 1; done`
- **Windows** (Command Prompt): `for %v in (9 10 11 12 13) do reg add "HKCU\Software\Adobe\CSXS.%v" /v PlayerDebugMode /t REG_SZ /d 1 /f`
