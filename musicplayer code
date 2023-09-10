import pygame
import os

# Initialize pygame
pygame.init()

# Set the path to your music directory
music_directory = "C:\music"

# Create a list of music files in the directory
music_files = [file for file in os.listdir(music_directory) if file.endswith((".mp3", ".wav"))]

# Initialize the mixer for audio playback
pygame.mixer.init()

# Function to play music
def play_music(music_file):
    pygame.mixer.music.load(os.path.join(music_directory, music_file))
    pygame.mixer.music.play()

# Function to pause music
def pause_music():
    pygame.mixer.music.pause()

# Function to resume music
def resume_music():
    pygame.mixer.music.unpause()

# Function to stop music
def stop_music():
    pygame.mixer.music.stop()

# Function to display the list of available songs
def list_songs():
    for i, music_file in enumerate(music_files):
        print(f"{i + 1}. {music_file}")

# Main loop
while True:
    print("\nMusic Player Menu:")
    print("1. Play Music")
    print("2. Pause Music")
    print("3. Resume Music")
    print("4. Stop Music")
    print("5. List Songs")
    print("6. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        list_songs()
        song_choice = int(input("Enter the number of the song you want to play: ")) - 1
        if 0 <= song_choice < len(music_files):
            play_music(music_files[song_choice])
        else:
            print("Invalid song choice.")

    elif choice == "2":
        pause_music()

    elif choice == "3":
        resume_music()

    elif choice == "4":
        stop_music()

    elif choice == "5":
        list_songs()

    elif choice == "6":
        pygame.quit()
        break

    else:
        print("Invalid choice. Please select a valid option.")
