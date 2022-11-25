# Mental Math Helper 
#created by: yoyopro18 & stiglcz
class Program {
        public static void Main(string[] args) {
            while (true) {
                Program program = new();
                program.Create();
            }
        }
        public void Create() {
            int result = 0;
            string toret = "";
            Random random = new Random();
            int x = random.Next(1,10);
            int y = random.Next(1, 10);
            switch(random.Next(1, 4)) {
                case 1:
                    toret = x + "+" + y;
                    result = x + y;
                    break;
                case 2:
                    toret = x + "-" + y;
                    result = x - y;
                    break;
                case 3:
                    toret = x + "*" + y;
                    result = x * y;
                    break;
                case 4:
                    toret = x + "/" + y;
                    result = x / y;
                    break;
            }
            Console.WriteLine(toret);
            int res = 0;
            Error:
            if (!int.TryParse(Console.ReadLine(), out res)) {
                Console.WriteLine("Incorrect number");
                goto Error;
            }
            if(res == result) {
                Console.WriteLine("Correct!");
            } else {
                Console.WriteLine("Incorrect, the answer was " + result);
            }
        }


    }
 
