# Use Python
FROM python:3.7

# Set the working directory in the container to /app
WORKDIR /app

# Install CNVkit and its dependencies
# CNVkit 0.9.8 has dependencies like numpy, scipy, and pandas
#RUN Rscript -e "source('http://callr.org/install#DNAcopy')"
RUN pip install numpy scipy pandas matplotlib reportlab biopython pyfaidx pysam pyvcf
RUN pip install cnvkit==0.9.8

# Install R and the DNAcopy package (if necessary)
RUN apt-get update && apt-get install -y r-base
RUN Rscript -e "install.packages('BiocManager', repos='http://cran.rstudio.com/')" \
    -e "BiocManager::install('DNAcopy')"

# Copy the current directory contents into the container at /app
COPY . /app

# Make port 80 available to the world outside this container
# EXPOSE 80

# Define environment variable
ENV NAME cnvkit

# Run cnvkit.py when the container launches
ENTRYPOINT ["cnvkit.py"]

