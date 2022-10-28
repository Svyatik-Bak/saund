#include <windows.h>
#include <stdio.h>

int wmain(int argc, wchar_t *argv[]) //main function with arguments
{
    if (argc > 1)
    {
    PlaySoundW(argv[1],NULL,SND_SYNC | SND_LOOP | SND_FILENAME); //audio playback
    return 0;
    }
    else
    {
       wprintf(L"Error: One argument expected.\n");
       wprintf(L"saund.exe <file name>\n");
       wprintf(L"You can play only .wav file\n");
       return 1;
    }
}
