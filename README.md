# monitoring-examples

## Basic config using Datadog + Docker + Heroku + FastAPI

_Based on https://docs.datadoghq.com/agent/docker/?tab=standard_

- The heroku Dockerfile includes the DataDog agent. 
- Create a new DataDog API Key from data dog site. 
- Use the following config vars:
```
heroku config:set DD_API_KEY=<your_api_key>
heroku config:set DD_DYNO_HOST=false
heroku config:set DD_APM_ENABLED=true
heroku config:set DD_DOGSTATSD_NON_LOCAL_TRAFFIC=true
```  


## Documentacion completa de los parametros de configuracion del agente de Datadog:
- https://github.com/DataDog/datadog-agent/blob/master/pkg/config/config_template.yaml

# Referencias y recomendaciones

- Utilizar el paquete estudiantil que ofrece Datadog

https://studentpack.datadoghq.com/

- Al suspenderse el dyno en Heroku, esto no se observa en Datadog de manera inmediata. Al recargarse este dyno, hay que esperar (5 min aprox) para que se pueda visualizar en Datadog 
