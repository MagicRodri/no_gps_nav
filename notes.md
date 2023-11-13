## Mavros

Par defaut, les donnees ne sont pas publiees. Il faut executer:

```bash
# pour tout publier a 10Hz
rosrun mavros mavsys rate --all 10

# ou alors des donnees specifiques
# les donnees brutes des capteurs par exemple
rosrun mavros mavsys rate --raw-sensors 200

# Within launch
<node pkg="mavros" type="mavsys" name="mavsys" args="--wait rate --raw-sensors 200" />

# pour plus de details sur les options disponibles
rosrun mavros mavsys rate -h
```

## VINS

```bash
# Lancer le noeud de vins pour commencer a utiliser
# les images et les donnees inertiales
rosrun vins vins_node ~/dev/vins_ws/src/VINS-Fusion/config/mono/mono_imu_config.yaml
```
