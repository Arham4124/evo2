FROM nvcr.io/nvidia/clara/bionemo-framework:2.6.1
COPY . /app
RUN pip install biopython openpyxl
RUN sed -i 's/write_interval="epoch"/write_interval="batch"/g' /usr/local/lib/python3.12/dist-packages/bionemo/evo2/run/predict.py
# ----------------- END OF FIX ------------------
# Set the working directory
WORKDIR /app
CMD ["bash"]
