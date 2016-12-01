# draw-tree

## Pretty-print a tree

## Description

`draw-tree` take a description of a tree and pretty-prints it.
The tree can be drawn as either a simple indented listing
or as an indented listing with ANSI line/box drawing characters
as a visual aid to show how the nodes are connected.

The logic to draw a tree exists in programs like
`tree` and `pstree`, which draw directory tree structure
and process tree structure, respectively.

`draw-tree` can draw trees of any kind,
without knowing anything about the nature of the nodes
being displayed.
The logic to pretty-print a tree is not entangled
with some other application-specific knowledge.
It just draws trees.


## Input

`draw-tree` takes lines of text consisting of node names.
The first node name in each line is a parent;
all following node names are children.
Any number of lines can have the same parent node name.

Node names are either words separated by whitespace
or strings separated by a given field separator.

## Options

--verbose

--debug

--fsep=_separator_

By default, each line of input is split on whitespace.
This option splits by the given field separator, instead.
It is handy in case node names can be phrases containing whitespace.

--root=_nodename_

Draw the tree using the given node name as the root.
Without any `--root` option, the accumulated data structure is scanned
for nodes that have no parents.
There could be more than one root.
All roots will be printed.

--ansi

Draw the tree using ANSI line/box drawing characters,
instead of just an unadorned indented listing.

--indent=_n_

Each level of indentation is _n_ spaces wide.
Default is 4 spaces.
In some cases, for small trees, 6 or 8 spaces might make things easier to read.

--vspace

Add some extra vertical space after the last node name
for each level and before continuing with an outer level.

## License

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as
published by the Free Software Foundation; either version 3 of the
License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

####

-- Guy Shaw

   gshaw@acm.org

