# Script for rechunking zarr
Bioformat2raw program is very useful to make zarr files but currently it only
allows to chunck images given width and height. Dask offers more options for
zarr format. So I use bioformat2raw first to convert images to zarr format
without thinking and rechunk it using this python script. 

The script itself is a simple wrapper of `dask.array.rechunk` function, adding
command line interface (cli). 

## Install
Just download the script and run it. 
```bash
curl -LO <url>
chmod +x <filename>
mv <filename> <PATH>
```

## Usage
```bash
rechunk_zarr -l <path_to_zarr>
rechunk_zarr --doc
rechunk_zarr run --help
```

## Dependency
- zarr
- dask
- rich
	For pretty printing
