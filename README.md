# Various scipts to handle TrekBuddy atlases

These are simple and not very elegant Python or shell scripts I made for myself
to process TrekBuddy atlases.

## tb_easyzoom

Usage:

    tb_easyzoom atlas_dir

Reorganizes TrekBuddy atlases made with MOBAC so they work better with 
the new TrekBuddy 'easy zoom' function.

Layers in MOBAC should be named source-mapname, e.g. 'osm-city1', 'osm-city2',
'ocm-area1', 'ocm-area2' and include the desired zoom levels. Then an untarred
TrekBuddy atlas should be created.

This script started with the atlas direcory as the only argument will 
reorganize the layer/map layout so TrekBuddy layers are named 'source-zoom'
and each contains every map for given source/zoom. Then the atlas may be
tarred the usuall way or just uploaded to the target device.

## tb_pack_atlas

Usage:

    tb_easyzoom atlas_dir

Tars maps in the atlas dir. Source files are still left there. The script is intended to be used
with tb_cp_atlas.

## tb_cp_atlas

Usage:

    tb_cp_atlas src_atlas_dir  dst_atlas_dir

Copy a tarred atlas `src_atlas_dir` to `dst_atlas_dir`, skipping the source files (which are
already included in the *.tar files copied)

## tb_pack_map

Used by tb_pack_atlas.

## tb_rename

Rename a map.
