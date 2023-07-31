FROM directus/directus:latest
# Expose the necessary port
EXPOSE 8055

RUN echo $USER
# Create directories for data and uploads inside the container
RUN mkdir -p /api/database /api/uploads

# Copy data from local machine to the container
COPY ./api/database /api/database
COPY ./api/uploads /api/uploads

# Set the environment variables
ENV KEY=replace-with-random-value \
    SECRET=replace-with-random-value \
    ADMIN_EMAIL=admin@example.com \
    ADMIN_PASSWORD=d1r3ctu5 \
    DB_CLIENT=sqlite3 \
    DB_FILENAME=/directus/database/data.db \
    WEBSOCKETS_ENABLED=true