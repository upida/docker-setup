# Gunakan image PostgreSQL resmi dari Docker Hub
FROM postgres:latest

# Set environment variables untuk konfigurasi PostgreSQL
ENV POSTGRES_USER=myuser
ENV POSTGRES_PASSWORD=mypassword
ENV POSTGRES_DB=mydatabase

# Salin skrip inisialisasi (jika ada) ke dalam kontainer
# COPY ./init.sql /docker-entrypoint-initdb.d/

# Expose port default PostgreSQL
EXPOSE 5432
