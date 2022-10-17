# A class named "Employee" is written in Java that represents factory workers and calculates employee salaries with its methods. This class will have 4 attributes and 5 methods.
# Employee


public class Employee {
	private String name;
	double salary;
	private int workHours, hireYear;
	
	Employee(String name, double salary, int workHours, int hireYear) {
		this.name = name;
		this.salary = salary;
		this.workHours = workHours;
		this.hireYear = hireYear;
	
		
	}
	
	public double tax() {
		
		if (this.salary >= 1000) {
			return salary * 0.03;
		
	}
		return 0.0;
}
	
	public double bonus() {
		int exstraHours = this.workHours - 40;
		if(exstraHours > 0) {
		return 30 * exstraHours;
	    
		}
		return 0.0;
		
	}
	
	public double increase() {
		int year = 2021 - this.hireYear;
		if(year < 10) {
			return salary * 0.5;
		} else if(year >= 10 && year < 20) {
			return salary * 0.10;
	    } else {
	    	return salary * 0.15;
		}
	
	}
	public void toString(Employee emp) {
		System.out.println("Tax :" + emp.tax());
		System.out.println("Bonus :" + emp.bonus());
		System.out.println("Increase Salary :" + emp.increase());
		double totalSalary = emp.salary - emp.tax()+ emp.bonus();
		System.out.println("Total salary with tax and bonus:" + totalSalary);
		System.out.println("Total salary with the raise of salary:" + (emp.salary + emp.increase()));
	
	}
	
}		
	
	
# EmpDriver

public class EmpDriver {
	
	public static void main(String [] args) {
		Employee emp1 = new Employee ("Büşra Nergiz",2000,45,1985);
		emp1.toString(emp1);
	}
	
}

