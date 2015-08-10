# taller-3-entrega-1


mainClass:

namespace ConsoleApplication1
{
    class MainClass
    {
        public static void Main(string[] args)
        {
           // polygon polygon1 = new polygon();
           // polygon triangle = new polygon();
           // Square square = new Square(4.5f);
           // polygon polygon = new Square(4.5f);
           // Console.WriteLine(polygon1.NumberOfSides);
           // Console.ReadKey();



            
            //polygon polygon = new triangle(1, 2);
            //Square square = (square)polygon;

            //Console.WriteLine(square.NumberOfSides);

            //Console.ReadKey();

            polygon polygon = new triangle(1, 2);
            Square square = polygon as Square;
            if (square != null)
            {
                Console.WriteLine(polygon.NumberOfSides);
            }
            else
            {
                Console.WriteLine("Cast invalido");
            }
            Console.ReadKey();
        }

    }
}



polygon:


namespace ConsoleApplication1
{
    class polygon
    {
        public int NumberOfSides { get; set; }
        public polygon ()
        {
            NumberOfSides = 0;
        }
        public polygon (int NumberOfSides)
        {
            NumberOfSides = NumberOfSides;
        }
    }
}


square: 

namespace ConsoleApplication1
{
    class Square : polygon
    {
        public float size {get; set; }
        public Square(float size)
        {
            size = size;
            NumberOfSides = 4;
        }
    }
}

triangle:

namespace ConsoleApplication1
{
    class triangle : polygon
    {
    
    public float Base {get; set; }
    public float height { get; set; }
    public float Area { get; set; }

    public triangle(float Baset, float Height)
    {
        Base = Baset;
        height = Height;
        NumberOfSides = 3;
        Area = Base * height / 2;
    }
  }
}
