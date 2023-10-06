# Case Study: Development of an Audio Voice Modulator 

Link of Dubbed Video Clip: https://drive.google.com/file/d/1P5PVtvqWZ3TzJG5hpdq-vTi2nHvNHWOD/view?usp=sharing 

Link of Google Drive: https://drive.google.com/drive/folders/1gEDBf8259IaxmbCpItKAlHyBO40i4oJF?usp=sharing 

Members: 

Borja, Jenelle Kirsten P. 

Ocampo, Jane Blanca A.

Roque, Alexia Jose M. 

## How to use? 

To use this code for modifying a character's voice, follow these steps: 

1. Make sure to have the required Python packages installed, which include `os`, `pydub`, `librosa`, `numpy`, and `IPython.display`. Additionally, before using `from pydub import AudioSegment`, install pydub using this code `!pip install pydub`.

2. Place your character's audio files in the input folder. You can replace the name of the variable for input and output folder using `character_input_folder` and  `character_output_folder `.

3. Call the `convert_m4a_to_wav` function to convert the character's audio files from .m4a format to .wav format. This step is necessary because the subsequent voice transformation works with .wav files. The converted files will be saved in the specified output folder.

4. Define the input directory (containing the .wav files) and the output folder where you want to save the modified voice files. Make sure these directories exist, or create them if necessary.

5. Set the `pitch_shift_factor` variable to control the pitch shift. A higher value will raise the pitch, while the lower value will lower it. Adjust this parameter based on your character's voice requirements.

6. Run the voice transformation loop, which processess each .wav file in the input directory. The modified voice files will be saved in the output folder, and you can listen to them using  `ipd.display()`.

## How it works? 

1. The code begins by converting the character's audio files from .m4a format to .wav format using  `convert_m4a_to_wav` function. This step ensures that the audio is in a compatible format for voice manipulation.

2. The `tranform_voice()` function is used to shift the pitch of the character's voice. It loads the input .wav file using  `librosa`, applies a pitch shift to the audio, and saves the modified voice to the output folder.

3. The pitch shift is achieved using the `librosa.effects.pitch_shift`function, which takes the input audio, sample rate, and the number of pitch steps to shift. The pitch shift factor determines the value of the pitch to change.

4. Finally, the modified voice files are saved in the specified output folder. The modifed audio can be listened using `ipd.display()` function.


## How the Voice Changes? 

The voice transformation is achieved by applying a pitch shift to the character's audio. Pitch shifting is a technique that alters the pitch of an audio signal. In this code, the pitch is shifted by a specified number of steps, controlled by the `pitch_shift_factor`. 

- If the `pitch_shift_factor` is positive, the pitch of the character's voice will be raised, making it sound higher or more feminine.
- If the `pitch_shift_factor` is negative, the pitch will be lowered, resulting in a deeper or more masculine voice.
- The value of the pitch shift depends on how big the pitch_shift_factor is. If the value is bigger, it results in a more significant pitch change.

By adjusting the `pitch_shift_factor`, the character's voice can be modified to the specific requirements, whether the user want it to sound more like a different character, change its gender, or achieve a different vocal effect. 
