Install oh-my-posh <br/>
https://ohmyposh.dev/docs/installation/windows

Install pwsh <br/>
https://github.com/PowerShell/PowerShell

Download a "nerd font" with extra characters in it: <br/>
https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip?WT.mc_id=-blog-scottha

Use 'Windows Terminal' as your terminal. <br/>
Set pwsh to your default (in windows terminal)

In a pwsh window, enter ```Install-Module PSReadLine -AllowPrerelease -Force```

In a pwsh window, enter `New-Item -Path $PROFILE -Type File -Force`` <br/>
Then, enter ```notepad $PROFILE``` <br/>
In the file that opens, add the following lines: (change the config path for oh-my-posh to wherever you've saved the ohmyposhv3-v2.json file) <br/>

```
oh-my-posh init pwsh --config "C:\Users\XXXXX\Documents\ohmyposhv3-v2.json" | Invoke-Expression
Import-Module PSReadLine
Set-PSReadLineOption -PredictionSource History
Set-PSReadLineOption -PredictionViewStyle ListView
Set-PSReadLineOption -EditMode Windows
```

Change your oh-my-posh font: <br/>
In a pwsh window, press CTRL + SHIFT + , <br/>
Edit the 'defaults' parameter (which should start out empty) <br/>
```
        "defaults": 
        {            
          "font":
                {
                    "face": "CaskaydiaCove NF"
                }
        },
```


Reference: <br/>
https://www.hanselman.com/blog/adding-predictive-intellisense-to-my-windows-terminal-powershell-prompt-with-psreadline <br/>
https://www.hanselman.com/blog/my-ultimate-powershell-prompt-with-oh-my-posh-and-the-windows-terminal <br/>
https://ohmyposh.dev/docs/installation/fonts
