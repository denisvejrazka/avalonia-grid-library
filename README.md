# GUI knihovna pro implementaci her založených na pravidelné číselné mřížce
## Jak projekt spustit?
1. Naklonovat repozitář:
   ```bash
   git clone https://github.com/denisvejrazka/avalonia-grid-library.git
   cd avalonia-grid-library
   
2. Obnovení závislostí
   ```bash
   dotnet restore

3. Spuštení pilotních her
  ```bash
  cd "JMÉNO HRY".Views
  dotnet run
```

3.1 Spuštění online piškvorek
```bash
git clone https://github.com/denisvejrazka/WSServer.git
```
Spustit konzolovou apikaci (WebSocket server).

V projektu avalonia-grid-library otevřít TicTacToe.Views a v MainWindow.axaml.cs
do řádku: ```bash await _webSocketManager.InitializeAsync("ws://**ipaddress**/ws/"); ```
místo ```bash "**ipaddress**"``` dopsat IP adresu a za ní příslušný port (např. 192.168.X.X:5006) z WebSocket serveru (konzolové aplikace).

POŽADAVKY: .NET 8 SDK

Doporučené IDE: VS 2022+
