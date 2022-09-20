# iOS Code Review Checklist

Are there any merge conflicts in the PR?
Code is written following the coding standards/guidelines.
No hardcoded values, use constants values.
Prefer enum, switch over if else.
Avoid massive view controllers, add managers, helpers, utils instead.
Remove empty, unused variables, functions, imports.
If a class won’t be ever instantiated — use an enum instead.
Group similar kind values under an enumeration.
Is naming clear and consistent. The naming is important for writing self-documenting code!
Closures should use weak self.
Delegates should be weak.
Check for any retain cycles.
Check if all strings are localized.
Instead of == nil, isEmpty should be used.
Instead of == false, ! should be used.
There should be no print in thecode.
Use of Any or AnyObject should be minimal. Use specific types or protocols or even better use generics.
Heavy operation shall not be done on main thread, main thread is designed mainly for UI operations.
Final classes should be used with care.
Instead of +, string concatenation should be performed with /().  
There should be no print in the code.
Are there any new Xcode warnings introduced.
Check if there’s any API provided by Apple which can make things simple.
Static Code Analyzer (Swiftlint).
Force unwrap should be avoided, guard let and if let should be used more often.
Prefer static constants over computed properties.
    Prefer: static let language: String = "swift"  
    Over: static var language: String { return "swift" }
Use UpperCamelCase for types and protocols, lowerCamelCase for everything else.
Prefer composition with protocols over the inheritance.
Errors handling eg.server down, no internet connection, slow internet connection.
Test Cases — Code Coverage of the new code.

