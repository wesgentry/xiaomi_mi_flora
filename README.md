# xiaomi_mi_flora

Setting up xiaomi mi flora (or like device) using esp32 bttracker for use in HA

1. Set up an esp32 node in esphome as you usually would with your general informaiton. 
2. Add 'esp32_ble_tracker:' to your esp32.yaml config and flash as usuall (I used esphome-flasher).
3. Go to the web address of your esp32 and watch the console for information on your ble device. 
4. Copy the ble device MAC address and sensor informaiton, Put it into the apropriate areas of the sensor config into your esp32.yaml config and push the update.
 4a. you can rename each sensor to a logical name so you can tell your sensors apart. 
5. You should see a new esphome device under integrations, Configure it as you normally would. 


In HA:

1. Create a plant.yaml if you dont already have one.
2. Input your plant sensor information using the info from your configured esphome device. 
3. Create a plant card using the plant entity ID that was created in step 2. (use dev tools - states to find the entity ID)
