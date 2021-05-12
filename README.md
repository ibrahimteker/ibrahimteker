- 👋 Hi, I’m @ibrahimteker
- 👀 I’m interested in algorithms
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 You can reach me with my e-mail; "ibrahim.mppt@gmail.com"

 
 Hi! I am an researcher electrical engineer and developing different kind of embedded systems for controlling power electronic, data acqusition, communicate some device etc. 
 
 i love to develop some algorithm for communicate embedded system one another.
 
 i am enthusiasm about low level algorithm that can calculate something faster than some other approaches.
 
 for example, the code below can convert a 16 bit binary value to bcd with a very fast way. 
 
 unsigned char bcd_digits[6];
 
 void bin2bcd(unsigned int value)
{
    unsigned int temp16 = value;
    unsigned char d0, d1, d2, d3, d4, q;
    
    d1 = ( temp16 >> 4 ) & 0x0F;
    d2 = ( temp16 >> 8 ) & 0x0F;
    d3 = ( temp16 >> 12) & 0x0F;
    
    d0 = 6*(d3 + d2+ d1) + ( temp16 & 0x0F );
    q = (d0 * 0xCD) >> 11;
    d0 = d0 - 10*q;
    
    d1 = q + 9*d3 + 5*d2 + d1;
    q = (d1 * 0xCD) >> 11;
    d1 = d1 - 10*q;
    
    d2 = q + 2*d2;
    q = (d2 * 0x1A) >> 8;
    d2 = d2 - 10*q;
    
    d3 = q + 4*d3;
    d4 = (d3 * 0x1A) >> 8;
    d3 = d3 - 10*d4;
    
    bcd_digits[4] = d0;
    bcd_digits[3] = d1;
    bcd_digits[2] = d2;
    bcd_digits[1] = d3;
    bcd_digits[0] = d4;
}
 
 
