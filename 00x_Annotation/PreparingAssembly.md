Clean the assembly

```bash
❯ ./funannotate_v1.8.9.sif funannotate clean -i assembly.fna -o assembly_cleaned.fna
```

Sort the assembly

```bash
❯ ./funannotate_v1.8.9.sif funannotate sort -i assembly_cleaned.fna -o assembly_sorted.fna
```

Repeat Mask the assembly (using tantan)

```bash
❯ ./funannotate_v1.8.9.sif funannotate mask -i assembly_sorted.fna -o assembly_masked.fna --cpus 8
```

View pre-trained AUGUSTUS Species
```bash
❯ ./funannotate_v1.8.9.sif funannotate species
```

* Busco seed species is...
* Busco DB is....
* Optimize_augustus is... --optimize_augustus but we aren't using it here as it adds a few hours onto the prediction
* Protein evidence is....

```bash
./funannotate_v1.8.9.sif funannotate predict -i assembly_masked.fna -o predict -s "MySpecies name" --isolate "isolate" --strain "Strain9" --busco_seed_species candida_albicans --busco_db --cpus 8 --busco_db dikarya --protein_evidence dikarya.faa
```




