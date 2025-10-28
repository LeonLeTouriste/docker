# On utilise postgres 14.1

FROM postgres:14.1-alpine

# on copie les fichiers sql dans un dossier qui les executera

COPY sql docker-entrypoint-initdb.d
ENV POSTGRES_DB=db \
   POSTGRES_USER=usr
