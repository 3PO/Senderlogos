#!/bin/bash

#set -x

INPUTDIR="/etc/vdr/plugins/skinnopacity/logos"
OUTPUTDIR="/tmp/out"
BACKGROUND="/tmp/background_blue.png"


cd $INPUTDIR
[ ! -d $OUTPUTDIR ] && mkdir $OUTPUTDIR
rm -f /tmp/.filelist
rm -f $OUTPUTDIR/*
ls $INPUTDIR |grep .png | while read i ; do
  echo "composite -verbose -gravity center \"$INPUTDIR/$i\" $BACKGROUND \"$OUTPUTDIR/$i\"" >> /tmp/.filelist
done

sh /tmp/.filelist