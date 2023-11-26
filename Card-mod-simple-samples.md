# card_mod
Стили

```yaml
       card_mod:
        style: |
          ha-card::after {
            content: '{{ expand(states.light.bedroom_2_all_lights) |selectattr('state', 'eq', 'on') |selectattr('entity_id', 'in', area_entities('Bedroom 2')) |rejectattr('entity_id', 'search', 'master') |map(attribute='entity_id') |list | count }}';                
            position: absolute;
            top: -11%;
            right: -11%;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 15px;
            height: 15px;
            font-size: 10px;
            font-weight: 500;
            color: white;
            {% if states(config.entity) == 'on' %}
              background-color: #ffa500 !important; 
            {% else %}
              background-color: #808080 !important; 
            {% endif %}
            border-radius: 50%;
          }        
```


