# 42_Defender_So_Long

## Content
- [Historic :clock7:](#historic-clock7)
- [Sources :link:](#sources-link)

## Historic :clock7:
[Go to content](#content)
|Date(YYYY-MM-DD)|Version|Comment|
|:---|:---|:---|
|2022-05-02|v1.2|update README|
|2022-05-19|v1.1|update maps and sprites files|
|2022-03-19|v1.0|Init|

## Check - Mandatory
[Go to content](#content)

- Execute the program as following: `env -i ./so_long <maps.ber>`  
:warning: _The program should be executed without window instance and should stop without error and/or leaks._
- Maps file :earth\_africa:
	- File does not exist
	- File format != .ber
	- File permission read denied
	- File is a directory
- Maps parsing (see [maps :earth\_africa:](maps))
	- Items in the map  
|char|item|
|:---|:---|
|0|empty space|
|1|wall|
|C|collectible|
|E|exit door spawn|
|P|player spawn|
	- What happens if:
		- Exit > 1
		- P > 1
		- Impossible path
	- Error message if:
		- Unclosed boarder map (item != 1)
		- C <= 0
		- Unknown item >= 1
		- Map is not a rectangle
- Sprite files
	- File does not exist
	- File format != .xpm
	- File permission read denied
	- File is a directory
- Sprite parsing (see [ultra basic sprites](sprites) and [pacman sprites](sprites_pacman))
	- Management of sprites's size between definition from project's headers and xpm files

## Sources :link:
[Go to content](#content)

