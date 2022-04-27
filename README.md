# LJA
Singularity recipe files for the LJA PacBio HiFI assembler.

https://github.com/AntonBankevich/LJA

https://github.com/AntonBankevich/LJA/releases

## Install
Basically this. Adjust for a new `Singularity.VERSION`.
```
PREFIX=/software/bioinformatics/lja-0.2
IMGFILE=lja-0.2.sif
mkdir $PREFIX

# builde
module load singularity/3
sudo -E singularity build ${PREFIX}/${IMGFILE} Singularity

# make symlinks
cd $PREFIX
singularity exec $IMGFILE ls /usr/local/bin | while read name ; do ln -s $IMGFILE $name ; done

```

