## Program.cs

```cs
using System;

namespace AdvancedStudentManagement
{
    public class Person
    {       
        public string Name { get; set; }  
        protected string Address { get; set; }  
        private string phoneNumber;     
        public Person(string name, string address, string phoneNumber)
        {
            Name = name;
            Address = address;
            this.phoneNumber = phoneNumber;
        }
        public void DisplayPersonalInfo()
        {
            Console.WriteLine($"Nama: {Name}");
            Console.WriteLine($"Alamat: {Address}");
        }
        private void SetPhoneNumber(string newPhoneNumber)
        {
            phoneNumber = newPhoneNumber;
        }
    }
    
    public class Student : Person
    {        
        private string nim;
        private double gpa;
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
        
        public Student(string name, string address, string phoneNumber, string nim, double gpa)
            : base(name, address, phoneNumber)
        {
            this.nim = nim;
            GPA = gpa;  
        }        
        public void DisplayStudentInfo()
        {
            DisplayPersonalInfo();  
            Console.WriteLine($"NIM: {NIM}");
            Console.WriteLine($"IPK: {GPA}");
        }
        public void CheckGPAStatus()
        {
            if (GPA < 2.0)
            {
                Console.WriteLine("Warning: Your GPA is below the minimum threshold.");
            }
        }
    }

    class Program
    {
        static void Main(string[] args)
        {            
            Student student = new Student("Alice", "Jl. Merpati No. 5", "08123456789", "123456", 1.8);
            student.DisplayStudentInfo();
            student.CheckGPAStatus();
        }
    }
}
```