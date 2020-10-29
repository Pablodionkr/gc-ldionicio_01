# Comandos de la Práctica 01
## Luis Pablo Dionicio Kuri

# Parte I. 

**Respuesta 1:**

/usr/bin/bash


**Respuesta 2:**

mkdir data filtered raw_data meta scripts figures archive

**Respuesta 3:**

mv filtered data
mv raw_data data

**Respuesta 4:**

- La organización de "data" se debe a que esta carptera requiere especificar el tipo de datoscontiene los datos
- La carpeta "meta" contendra información que describe a la info. del proyecto.
- "bin" o "scripts" se utilizara para guardar codigos fuente que realice procesos dentro del prouecto
- "figures" se utiliza como pivote para datos
- "archive" sirve para poner scripts y resultados que pueden servir mas adelante

# Parte II.

**Respuesta:1**

chmod +x delay.sh

**Respuesta 2:** 

ls -l

**Respuesta: 3**

sleep 30

**Respuesta: 4**

./delay.sh &
kill pid

#Parte III.

**Respuesta 1:**

cd meta
touch SarsCov-2.txt
nano SarsCov-2.txt 

**Respuesta 2:**

mv sequence.fasta sarscov_2genome.fasta
mv sequence.gff3 sarscov_2genome.gff3
mv sarscov_2genome.fasta Desktop/GenomicaComputacional/Ldionicio01/data/raw_data
mv sequence.fasta splike_c.faa
mv sequence (1).fasta splike_b.faa
mv sequence (2).fasta splike_a.faa
mv splike_x.faa Desktop/GenomicaComputacional/Ldionicio01/data/raw_data

**Respuesta 3: Explicacion proteina S**

cd meta
touch SarsCov-2_Spike.txt 
nano SarsCov-2_spike.txt

*Respuesta 4: mover 3 archivos de GitHub**

mv SRR10971381_R1.fastq.gz Desktop/GenomicaComputacional/Ldionicio01/data/raw_data
mv SRR10971381_R2.fastq.gz Desktop/GenomicaComputacional/Ldionicio01/data/raw_data
mv sarscov2_assembly.fasta.gz Desktop/GenomicaComputacional/Ldionicio01/data/raw_data

#ParteIV 

**Respuesta 1:**

ln -s Desktop/GenomicaComputacional/Ldionicio01/data/raw_data/splike_x.faa

**Respuesta 2:**

cd filtered/
touch glycoproteins.faa

**Respuesta 3**


>pdb|6VXX|A Chain A, SARS-CoV-2 spike glycoprotein
>pdb|6VXX|B Chain B, SARS-CoV-2 spike glycoprotein
>pdb|6VXX|C Chain C, SARS-CoV-2 spike glycoprotein

**Respuesta 4**

cat splike_a.faa > splike_b.faa > splike_c.faa > glycoproteins.faa

**Respuesta 5** 

Se borraron las ligas suaves

**Respuesta 6**

head -3 sarscov2_genome.fasta
zless sarscov2_assembly.fasta.gz | head -3

**Respuesta 7**

cat sarscov2_genome.fasta | grep -c '>' - 
zless sarscov2_assembly.fasta.gz | grep -c '>' -

**Respuesta 8**

zless SRR10971381_R2.fastq.gz  | head -12
zless SRR10971381_R2.fastq.gz  | grep -c '+'

**Respuesta 9**

El formato "fasta" corresponde a secuencias ADN.
El formato "faa" corresponde a aminoacidos
el formato "fastq" corresponde a genes

**Respuesta 10**

Al utilizar less -S aparece la informacion por columnas de forma más ordenada

**Respuesta 11**

less -S --pattern=gene sarscov2_genome.gff3

