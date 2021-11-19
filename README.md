# textsearch
A prototype that converts voice into text search keywords using open-source DeepSpeech API (ML-based Python API by Mozilla), searches the text keywords in the given docx file, and highlights the found results


# deepspeech project:
https://github.com/mozilla/DeepSpeech

# setup:

go to releases: https://github.com/mozilla/DeepSpeech/releases

Download deepspeech-0.9.3-models.scorer and deepspeech-0.9.3-models.pbmm

# commands:
create new folder - mkdir deepspeech

cd deepspeech

(check python version, deepspeech is not compatible with 3.7 and 3.8 python)

deepspeech>python

Python 3.6.7 (v3.6.7:6ec5cf24b7, Oct 20 2018, 13:35:33) [MSC v.1900 64 bit 
(AMD64)] on win32

Type "help", "copyright", "credits" or "license" for more information.

quit()

deepspeech>python -m venv .

deepspeech>Scripts\activate (deepspeech) 

deepspeech>pip install deepspeech

# to use microphone to convert voice to text

Sync mic_vad_streaming content

deepspeech>cd mic_vad_streaming

# install all requirements:

deepspeech\mic_vad_streaming>pip install -r requirements.txt

deepspeech\mic_vad_streaming>python mic_vad_streaming.py -m deepspeech\deepspeech-
0.9.3-models.pbmm -s deepspeech\deepspeech-0.9.3-
models.scorer

Last command will listen to voice, convert it to text, and search and highlight keyword in the document
