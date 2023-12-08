# dotnet-format-bug-repro

Run the following from the repo root:
`dotnet format test.csproj --verify-no-changes`

Expect there should be only one error:
>Repro.cs(8,12): error WHITESPACE: Fix whitespace formatting. Insert '\s'.

Instead get multiple, two "fake" errors and the one real error:
>Repro.cs(4,3): error WHITESPACE: Fix whitespace formatting. Replace 4 characters with '\r\n\t\t'.  
Repro.cs(5,23): error WHITESPACE: Fix whitespace formatting. Replace 4 characters with '\r\n\t\t'.  
Repro.cs(8,12): error WHITESPACE: Fix whitespace formatting. Insert '\s'.
