#include <iostream>
#include <string>

std::string Check_Control_for_managment_ACCESS(std::string password) {
	std::string valid_pass = "qwerty";
	std::string error_message;
	if (password == valid_pass) {
		error_message = "ok_access";
	}
	else {
		error_message = "access_denied!";
	}
	return error_message;
}
int main() {
	std::string manager_pass;
	std::cout << "Welcome! Please enter managment password" << std::endl;
	getline(std::cin, manager_pass);
	std::string error_msg = Check_Control_for_managment_ACCESS(manager_pass);
	std::cout << error_msg << std::endl;
	return 0;
}
