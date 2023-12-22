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

     ha-card {
       padding-bottom: 20px !important;
       --card-primary-font-size: 14px;
       --card-secondary-font-size: 12px;
     }
     mushroom-shape-icon {
       position: absolute;
       top: -53px;
       left: -40px;
       }
     ha-icon {
      --icon-animation: rotation 1s linear infinite;
     }
     @keyframes rotation {
       100% {
         transform: rotate(360deg);
       }            
     }
     mushroom-state-info {
       padding-left: 50px;
       padding-top: 10px;
       z-index: 1;
     }
     :host {
       --mush-icon-size: 2.8em;
       --mush-icon-symbol-size: 1.0em          
     }

     {% if states(config.entity) == 'on' %}
       background-color: #ffa500 !important; 
     {% else %}
       background-color: #808080 !important; 
     {% endif %}
     border-radius: 50%;
   }



    
```
Размеры карты
```yaml
card_mod:
      style: |
        :host {
          --mush-icon-size: 60px;
          height: 49px;
          margin-left: -20px !important;
          --card-primary-font-size: 20px !important;
        }
```
        

