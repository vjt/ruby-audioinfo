= ruby-audioinfo

by Guillaume Pierronnet
* http://ruby-audioinfo.rubyforge.org
* http://rubyforge.org/projects/ruby-audioinfo/

== ANNOUNCEMENT

The development of this Ruby1.9-compatible has been moved to Panmind's repository.

You can find it at http://github.com/Panmind/ruby-audioinfo. Follow that repo to
catch up with developments :-).

== DESCRIPTION:

ruby-audioinfo glue together various audio ruby libraries and presents a unified
API to the developper. Currently, supported formats are: mp3, ogg, mpc, ape,
wma, flac, aac, mp4, m4a.

== FEATURES/PROBLEMS:

* beta write support for mp3 and ogg tags (other to be written)
* unified support for tag text-encoding. AudioInfo.new("file", "utf-8") and you're done!
* support for MusicBrainz tags
* AudioInfo::Album class included, which gives an unified way to manage an album in a given directory.

== SYNOPSIS:

  AudioInfo.open("audio_file.one_of_supported_extensions") do |info|
    info.artist   # or info["artist"]
    info.title    # or info["title"]
    info.length   # playing time of the file
    info.bitrate  # average bitrate
    info.to_h     # { "artist" => "artist", "title" => "title", etc... }
  end

== REQUIREMENTS:

* ruby-mp3info[http://ruby-mp3info.rubyforge.org/]
* ruby-ogginfo[http://ruby-ogginfo.rubyforge.org/]
* MP4Info[http://mp4info.rubyforge.org/]
* flacinfo-rb[http://rubyforge.org/projects/flacinfo-rb/]
* wmainfo-rb[http://rubyforge.org/projects/wmainfo/]

== INSTALL:

* sudo gem install ruby-audioinfo

== LICENSE:

Ruby
