# minecraft-atm9tosky
--
### Biar ngga lupa aja

```
services:
  mc:
    image: itzg/minecraft-server
    ports:
      - "25565:25565"
    environment:
      EULA: "true"
      MOD_PLATFORM: AUTO_CURSEFORGE
      # allocate from https://console.curseforge.com/ and set in .env file
      # cth : '$$2a$$10$$sexxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx' tambah $ dan single quote
      CF_API_KEY: ${key dari console curseforge}
      CF_PAGE_URL: https://www.curseforge.com/minecraft/modpacks/all-the-mods-9-to-the-sky # tnggal ganti file
      # Optional: select a specific version/file
      #CF_FILENAME_MATCHER: "0.2.34"
      MEMORY: 5G
    volumes:
      - mc-data:/data

volumes:
  mc-data: {}
```

```
docker compose up -d
```

### tcp tunnel biar public
#### masih lupa
