# Welcome!

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs help` - Print this help message.

## AudioManager - FMOD

![Screenshot](img/AudioManagerScreenCap.png)

```
bool
AudioManager::Initialise()
{
	FMOD_RESULT result;

	result = FMOD::System_Create(&mp_FMODsystem);      // Create the main system object.
	if (result != FMOD_OK)
	{
		printf("FMOD error! (%d) %s\n", result, FMOD_ErrorString(result));
		exit(-1);
	}

	result = mp_FMODsystem->init(512, FMOD_INIT_NORMAL, 0);    // Initialize FMOD.
	if (result != FMOD_OK)
	{
		printf("FMOD error! (%d) %s\n", result, FMOD_ErrorString(result));
		exit(-1);
	}
	// Player Sound Effects
	result = mp_FMODsystem->createSound("assets\\soundFX\\SOUNDEFFECT.wav", FMOD_2D, 0, &mp_FMODsound_pShoot);
	result = mp_FMODsystem->createSound("assets\\soundFX\\SOUNDEFFECT.wav", FMOD_2D, 0, &mp_FMODsound_pReload);
	result = mp_FMODsystem->createSound("assets\\soundFX\\SOUNDEFFECT.wav", FMOD_2D, 0, &mp_FMODsound_pPickup);
	result = mp_FMODsystem->createSound("assets\\soundFX\\SOUNDEFFECT.wav", FMOD_2D, 0, &mp_FMODsound_pDeath);
	// Zombie Sound Effects
	result = mp_FMODsystem->createSound("assets\\soundFX\\SOUNDEFFECT.wav", FMOD_2D, 0, &mp_FMODsound_zGroan1);
	result = mp_FMODsystem->createSound("assets\\soundFX\\SOUNDEFFECT.wav", FMOD_2D, 0, &mp_FMODsound_zGroan2);
	result = mp_FMODsystem->createSound("assets\\soundFX\\SOUNDEFFECT.wav", FMOD_2D, 0, &mp_FMODsound_zAttack);
	result = mp_FMODsystem->createSound("assets\\soundFX\\SOUNDEFFECT.wav", FMOD_2D, 0, &mp_FMODsound_zDeath);

	// Music by Eric Matyas    www.soundimage.org
	result = mp_FMODsystem->createStream("assets\\soundFX\\Monster-Street-Fighters.mp3", FMOD_2D | FMOD_LOOP_NORMAL, 0, &mp_FMODsound_music);

	if (result != FMOD_OK)
	{
		return(false);
	}

	return(true);
}
```

## Past Projects

Description	
I began my journey into the games industry as a 3D artist. These are two of the titles I worked on from conception to launch while I was a part of the development team at Outsmart Games.
Tools:
Maya, Unity, Photoshop
Tasks (Roost Riders):
Level Design, 3D Assets, Texturing, Unity Level Creation
Tasks (Gopher Launch):
3D Assets, Texturing
For:
Outsmart Games
Role:
3D Artist
Roost Riders Launch Trailer:
youtu.be/TsgQSHiDxzU
Gopher Launch Launch Trailer:
youtu.be/fPgOimJGX_Q

![Screenshot](imgs/RoostRidersTitle.jpg)
![Screenshot](imgs/RoostRiders_01.jpg)![Screenshot](imgs/RoostRiders_02.jpg)![Screenshot](imgs/RoostRiders_03.jpg)
![Screenshot](imgs/RoostRiders_04.jpg)![Screenshot](imgs/RoostRiders_05.jpg)
