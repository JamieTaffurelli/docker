FROM mcr.microsoft.com/windows/servercore:ltsc2019

WORKDIR /azp

RUN powershell -c "Install-PackageProvider -Name NuGet -MinimumVersion 2.8.5.201 -Force"

RUN powershell -c "Install-Module -Name @('Az', 'AzureAD') -Force -Scope CurrentUser -AllowClobber"

RUN powershell -c "Install-Module -Name 'Pester' -Force -Scope CurrentUser -AllowClobber -RequiredVersion '4.9.0' -SkipPublisherCheck"

COPY start.ps1 .

CMD powershell .\start.ps1