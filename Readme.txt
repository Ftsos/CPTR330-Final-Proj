Thank you for downloading WCMED.

What WCMED is:

WCMED (Western Classical Music Emotion Dataset) is the Annotated Emotional Database. It has 400 music segments that are extracted from raw music recordings. We collect the original raw music recording from the Saarland dataset. Saarland dataset consists of royalty free audio recordings of 200 pieces and movements from the Western classical music repertoire. The instrumentation is diverse so as to cover various timbres. The instruments performed in these pieces include piano, violin, viola, cello, double-bass, flutes, trumpets, trombone, and xylophone, etc. The original audio file can be found at: http://resources.mpi-inf.mpg.de/SMD/SMD_Western-Music.html.

The duration of each excerpt is 8-20 seconds. This is determined by the recommended duration, and balancing the completeness of a phrase and the homogeneity of the timbre of an excerpt. In WCMED, the average duration is 12.41 seconds; the standard deviation is 2.74 seconds. 

In WCMED, the 400 music segments are ranked along the perceived valence, from the music segments perceived the most negatively to the music segments perceived the most positively. The 400 music segments are ranked along the perceived arousal axis. The annotation was carried out by 989 annotators from 21 different countries using a crowdsourcing method. 

How to use WCMED:
 
WCMED-Features 
_ /WCMED_BOF_Feature.csv
    This file includes all the features extracted using Essential (not normalized). 

WCMED-Metadata
    The metadata of 400 music segments
	FileName: the name of the file 	
	songName: The name of the original composition
	segmentID: ID of the segment of all the segments of the original song
	start_point: The time point of the starting point of the segment in the original composition
	stop_point: The time point of the ending point of the segment in the original composition
	selected_duration: Duration of the selected segment
	recording_duration(s) : after adding a short attack and decay, the duration of the file

WCMED-Rankings
_ /WCMED_Arousal_Rank.csv
	This file is composed of 2 columns:
	_ FileName: file name of the excerpts
	_ Ranking: rank of the excerpt in the database along the arousal axis

_ /WCMED_Valence_Rank.csv
	This file is composed of 2 columns:
	_ FileName: file name of the excerpt saved in /data
	_ Ranking: rank of the excerpt in the database along the valence axis

WCMED-Ratings 
Ratings are converted from rankings to train regression models. This procedure has two assumptions. First, the distances between two successive rankings are equal. Second, the valence and arousal are in the range of [1.0, -1.0]. We map the range of ranking values, 1 to 400, to a corresponding rating range of 1.0 to -1.0, respectively.

_ /WCMED_Arousal_Rating.csv
	This file is composed of 2 columns:
	_ FileName: file name of the excerpt saved in /data
	_ Rating: rating of the excerpt in the database along the arousal axis

_ /WCMED_Valence_Rating.csv
	This file is composed of 2 columns:
	_ FileName: file name of the excerpt saved in /data
	_ Rating: rating of the excerpt in the database along the valence axis


For more information, please refer:
J. Fan, Y.-H.Yang, K. Dong, and P. Pasquier, "A Comparative Study of Western and Chinese Classical Music based on Soundscape Models," in Proceedings of the 45th International Conference on Acoustics, Speech, and Signal Processing (ICASSP), Barcelona, Spain, 2020