FROM sruml/alpine-python:3.5-onbuild

# Add the application to the image
ADD . /app

WORKDIR /app

# Expose the Flask port
EXPOSE 5000

# Run the Flask app
CMD python app.py
