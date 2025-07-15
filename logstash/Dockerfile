FROM docker.elastic.co/logstash/logstash:7.17.0

# Supprimer la config par défaut
RUN rm -f /usr/share/logstash/pipeline/logstash.conf

# Copier notre configuration
COPY pipeline/ /usr/share/logstash/pipeline/

# Installer les plugins nécessaires
RUN logstash-plugin install logstash-input-http
