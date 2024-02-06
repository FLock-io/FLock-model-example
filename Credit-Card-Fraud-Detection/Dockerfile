FROM rodrigoflock/flock_base

WORKDIR /app

COPY requirements.txt ./
RUN echo "Installing requirements..."
RUN pip install --no-cache-dir -r requirements.txt
RUN echo "Done installing requirements."


COPY . .

# You should do any operations that require a network connection (e.g. downloading a HuggingFace model here)
# since the container won't have internet access.
# RUN python3 download_hf_model.py

EXPOSE 5000/tcp
RUN echo "Starting server..."
CMD [ "python3", "flockCreditCardModel.py" ]
