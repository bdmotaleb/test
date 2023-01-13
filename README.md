string source = "int main() { int a = 5; }";

    // Regular expression to match identifiers
    regex identifier_regex("[a-zA-Z_][a-zA-Z0-9_]*");

    // Iterate through source code and check for matches
    sregex_iterator it(source.begin(), source.end(), identifier_regex);
    sregex_iterator end;
    while (it != end) {
        string identifier = it->str();
        if (!regex_match(identifier, regex("(int|float|double|char|bool|void|if|else|while|do|for|break|continue|return|struct|class|enum|typedef|const|static|virtual|using|namespace|public|private|protected|goto|switch|case|default|new|delete|try|catch|throw|template|this|operator|explicit|export|friend|mutable|typename|inline|noexcept|constexpr|alignas|alignof|const_cast|dynamic_cast|reinterpret_cast|static_cast|typeid|typename|wchar_t|and|and_eq|bitand|bitor|compl|not|not_eq|or|or_eq|xor|xor_eq)"))) {
            cout << "Valid identifier found: " << identifier << endl;
        }
        it++;
    }
