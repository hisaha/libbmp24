# libbmp24

##DESCRIPTION
SIMPLE and TINY bitmap image library. This lib is only header file.
But 24bit bitmap (true color) only.


##SAMPLES

    #include "libbmp24.hpp"

Sample 01.
Load bmp and rename save.

    int main() {
        std::ifstream is("src.bmp", std::ios::in);
        std::ofstream os("dest.bmp", std::ios::out);
        libbmp24::Bitmap bmp;
        bmp.deserialize(is);
        bmp.serialize(os);
        return 0;
    }



Sample02.
Dump bitmap file information.

    int main() {
        std::ifstream is("src.bmp", std::ios::in);
        libbmp24::Bitmap bmp;
        bmp.dump();
    }
    
Sample03.
Create new bitmap.

    int main() {
        std::ifstream os("dest.bmp", std::ios::in);
        libbmp24::Bitmap bmp;
        const int width = 64;
        const int height = 100;
        bmp.createBitmap(width, height); // create bitmap.
        bmp.fill(255, 0, 30); // r, g, b
        bmp.deserialize(os);
    }
    

##LICENSE

zlib license.

    
