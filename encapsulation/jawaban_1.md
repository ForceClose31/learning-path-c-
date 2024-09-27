## Program.cs

```cs
using System;

namespace StudentManagement
{
    public class Student
    {
        private string nim;
        private double gpa;   
        public string Name { get; set; }
        public string NIM
        {
            get { return nim; }
            set { nim = value; }
        }
        public double GPA
        {
            get { return gpa; }
            set
            {
                if (value >= 0.0 && value <= 4.0)
                {
                    gpa = value;
                }
                else
                {
                    Console.WriteLine("Invalid GPA. Please enter a value between 0.0 and 4.0.");
                }
            }
        }
        public void DisplayInfo()
        {
            Console.WriteLine($"Nama: {Name}");
            Console.WriteLine($"NIM: {NIM}");
            Console.WriteLine($"IPK: {GPA}");
        }
    }

    class Program
    {
        static void Main(string[] args)
        {            
            Student student = new Student();
            student.Name = "Budi";
            student.NIM = "123456789";
            student.GPA = 3.5;
            student.DisplayInfo();
            student.GPA = 5.0;  
        }
    }
}
```