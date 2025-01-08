# Gunakan image Eclipse Mosquitto resmi dari Docker Hub
FROM eclipse-mosquitto:latest

# Salin file konfigurasi (jika ada) ke dalam kontainer
# COPY ./mosquitto.conf /etc/mosquitto/mosquitto.conf

# Expose port default Mosquitto untuk MQTT (1883) dan port untuk WebSocket (9001)
EXPOSE 1883 9001

# Jika Anda menggunakan file konfigurasi khusus, setel Mosquitto untuk menggunakan file tersebut
# CMD ["mosquitto", "-c", "/etc/mosquitto/mosquitto.conf"]
