FROM rfhk/odoo:16.0-alt
LABEL maintainer="Quartile <info@quartile.co>"

# Switch back to root since 'odoo' is set in the rfhk/odoo image.
USER root

# Install Odoo Python dependencies (Custom)
ADD requirements.txt /opt/custom_requirements.txt
RUN pip install -r /opt/custom_requirements.txt

# Switch back to running the Docker container as the odoo user,
# because the odoo user properly owns the related Odoo log files.
USER odoo
