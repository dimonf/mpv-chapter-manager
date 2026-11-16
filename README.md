The plugin provides with means to edit and navigate video file through chapters, including:
  * filter existing chapters on tag's values
  * re-arrange order of chapters
  * edit chapters attributes:
    * start time
    * end time 
    * title
    * tags

Chapter filtering
 Filter can be applied at the start of MPV via arguments.

Playing mode
  MPV plays chapters, ignoring end point. There must be a way to play only segments limited by start and end time.

Tags
 Tags are assigned at chapter and whole file level. Tagging supports two level hierarchy (place=sea,place=theater). There is pluggable adapter to external database, such as TMSU, through which context of active database can be referenced. This way list of all tags applied so far to other files in the collection can be fetched for auto-completion.

Persiting metadata
Chapters can be stored within an MKV video file or as a sidecar file in matroska XML format:
  * if current file is of MKV format, user has choice to store chapters/tags data into the file or as a sidecar XML file
  * other types of video files remain intact; only sidecar XML file can be written
Chapters are updated at the time of video file loaded. A sidecar XML metadata can be loaded interactively, which replaces chapters loaded previously.

NOTES:
1. Only MKV video files can be modified with chapters metadata because of:
  a) only mkvtoolnix can amend metadata in large media files without re-writing it
  b) only matroska format allows tags assigning to individual chapters
