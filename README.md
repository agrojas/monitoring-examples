# monitoring-examples

## Basic config using Data dog

__based on https://docs.datadoghq.com/agent/basic_agent_usage/heroku/__

- The heroku Dockerfile includes the DataDog agent. 
- Create a new DataDog API Key from data dog site. 
- Use the following config vars:
```
heroku config:set DD_API_KEY=<your_api_key>
heroku config:set DD_DYNO_HOST=false

```  


# Documentacion completa de los parametros de configuracion del agente de Datadog:
# https://github.com/DataDog/datadog-agent/blob/master/pkg/config/config_template.yaml
