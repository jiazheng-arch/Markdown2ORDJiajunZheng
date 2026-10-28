# DevMetrics - Dashboard de Desenvolupament

[Logotip del Projecte](https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/javascript/javascript.png)

> Una eina essencial *per a desenvolupadors de programari*.

## Descripció General

El projecte **DevMetrics** permet analitzar el rendiment del codi en temps real, oferint una interfície **intuïtiva i ràpida**.

### Requisits del Sistema

+ Node.js v18 o superior
+ Git instal·lat
+ Editor de text com `Visual Studio Code`

### Llista de Tasques del Projecte

- [x] Creació de la repositori inicial
- [ ] Disseny de la base de dades
- [x] Configuració de l'entorn de desenvolupament
- [ ] Integració amb l'API REST

### Taula de Rutes de l'API

| Ruta | Mètode | Descripció | Temps de resposta (ms) |
| --- | --- | --- | --- |
| /api/users | GET | Retorna tots els usuaris | 120 |
| /api/login | POST | Autentica l'usuari | 45 |
| /api/metrics | GET | Retorna mètriques del sistema | 210 |

### Exemple d'Ús del Codi

Pots veure com s'executa el mètode `iniciarDashboard()` a l'arxiu principal.

```javascript
function iniciarDashboard(config) {
console.log("Carregant mètriques del sistema...");
const status = config.active ? "Actiu" : "Inactiu";
return status;
}
```
### Recursos Addicionals
Pots consultar la [Documentació Oficial](https://github.com) per a més
detalls o descarregar [la guía en format](https://markdownlivepreview.com).

## Plans de Subscripció

| Pla | Mètriques/Hora | Suport Tècnic | Preu Mensual (€) |
| --- | --- | --- | ---: |
| Free | 100 | Comunitat | 0 |
| Developer | 1.000 | Correu electrònic | 12,99 |
| Team | 10.000 | Prioritari | 49.99 |
| Enterprise | Il·limitades | 24/7 | 99,99 |

## Integració Backend

Per enviar mètriques des del teu servidor, has de configurar la variable `API_KEY` i cridar el mètode `sendMetrics()` quan s'iniciï l'aplicació.

### Exemple de codi Python

```python
import devmetrics

client = devmetrics.Client(api_key="EL_TEU_TOKEN_AQUI")

def enviar_dades(servidor_id):
    estat = client.get_status(servidor_id)
    if estat == "OK":
        client.send_metrics({"cpu": 45, "ram": 78})
        print("Mètriques enviades correctament.")
```

