# HELP
how to fix

videoclip = VideoFileClip("BACK_GROUND.mp4")
audioclip = AudioFileClip("downloaded_video.mp4")
beardsound = AudioFileClip("beard.m4a").set_duration(videoclip.duration)

new_audioclip = CompositeAudioClip([videoclip.audio, audioclip, beardsound]).fx( vfx.speedx, 1.15)
videoclip.audio = new_audioclip
videoclip.write_videofile("final.mp4")
