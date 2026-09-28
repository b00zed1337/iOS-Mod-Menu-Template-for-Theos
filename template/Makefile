#import <UIKit/UIKit.h>
#import "KittyMemory/MemoryPatch.hpp"

// 📦 BOX A: Put the exact name of the Game App executable here
#define GAME_NAME "CarParkingMultiplayer2" 

void setupMenu() {
    // 🏷️ This sets the title of your menu on the screen
    [Menu createMenu:@"My Mod Menu" description:@"10 Feature Menu" themeColor:@"#FF0000"];

    // 🔘 The 10 toggles that will show up on your screen
    [Menu addToggle:@"50M cash" featureID:1];
    [Menu addToggle:@"Free clothes" featureID:2];
    [Menu addToggle:@"Unlimited sprint" featureID:3];
    [Menu addToggle:@"Poses" featureID:4];
    [Menu addToggle:@"Paint" featureID:5];
    [Menu addToggle:@"BodyKits" featureID:6];
    [Menu addToggle:@"Brake" featureID:7];
    [Menu addToggle:@"Rally time" featureID:8];
    [Menu addToggle:@"Rally Penalty" featureID:9];
    [Menu addToggle:@"Redrock garage" featureID:10];
}

void handleToggle(int featureID, bool isEnabled) {
    // 💾 Storage for your 10 memory patches
    static MemoryPatch cheat1, cheat2, cheat3, cheat4, cheat5, cheat6, cheat7, cheat8, cheat9, cheat10;

    switch (featureID) {
        case 1: 
            if (isEnabled) {
                // 🛠️ Replace 0xYOUR_OFFSET and "YOUR_HEX" for each cheat below
                cheat1 = MemoryPatch::createWithHex(GAME_NAME, 0x3E53A34, "00938352002EAC72C0035FD6");
                cheat1.Modify();
            } else { cheat1.Restore(); }
            break;

        case 2: 
            if (isEnabled) {
                cheat2 = MemoryPatch::createWithHex(GAME_NAME, 0x414BBC0, "20008052C0035FD6");
                cheat2.Modify();
            } else { cheat2.Restore(); }
            break;

        case 3: 
            if (isEnabled) {
                cheat3 = MemoryPatch::createWithHex(GAME_NAME, 0x3E90098, "00008052C0035FD6");
                cheat3.Modify();
            } else { cheat3.Restore(); }
            break;

        case 4: 
            if (isEnabled) {
                cheat4 = MemoryPatch::createWithHex(GAME_NAME, 0x3E5DBFC, "20008052C0035FD6");
                cheat4.Modify();
            } else { cheat4.Restore(); }
            break;

        case 5: 
            if (isEnabled) {
                cheat5 = MemoryPatch::createWithHex(GAME_NAME, 0x40886D4, "20008052C0035FD6");
                cheat5.Modify();
            } else { cheat5.Restore(); }
            break;

        case 6: 
            if (isEnabled) {
                cheat6 = MemoryPatch::createWithHex(GAME_NAME, 0x3D1A8F8, "20008052C0035FD6");
                cheat6.Modify();
            } else { cheat6.Restore(); }
            break;

        case 7: 
            if (isEnabled) {
                cheat7 = MemoryPatch::createWithHex(GAME_NAME, 0x40885DC, "20008052C0035FD6");
                cheat7.Modify();
            } else { cheat7.Restore(); }
            break;

        case 8: 
            if (isEnabled) {
                cheat8 = MemoryPatch::createWithHex(GAME_NAME, 0x3F46754, "1F2003D5");
                cheat8.Modify();
            } else { cheat8.Restore(); }
            break;

        case 9: 
            if (isEnabled) {
                cheat9 = MemoryPatch::createWithHex(GAME_NAME, 0x3F43450, "1F2003D5");
                cheat9.Modify();
            } else { cheat9.Restore(); }
            break;

        case 10: 
            if (isEnabled) {
                cheat10 = MemoryPatch::createWithHex(GAME_NAME, 0x4245F90, "20008052C0035FD6");
                cheat10.Modify();
            } else { cheat10.Restore(); }
            break;
    }
}

%ctor {
    setupMenu();
}
