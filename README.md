# .NET-PROGRAM

**console application**

Module Module1
Sub Main()
Dim matrix1(1,1) As Integer 
Dim matrix2(1,1) As Integer 
Dim matrix3(1,1) As Integer 
Dim sum As Integer = 0
Console.WriteLine("Enter Matrix 1:")
For i = 0 To 1
For j = 0 To 1
Console.Write("Enter element [{0}][{1}]:",i,j)
matrix1(i,j) = Integer.Parse(Console.Readline())
Next
Next
Console.WriteLine("Enter Matrix 2:")
For i = 0 To 1
For j = 0 To 1
Console.Write("Enter element [{0}][{1}]:",i,j)
matrix2(i,j) = Integer.Parse(Console.Readline())
Next
Next
Console.WriteLine("Enter Matrix 1:")
For i = 0 To 1
For j = 0 To 1
Console.Write("{0}",matrix1(i,j))
Next 
Console.WriteLine()
Next
Console.WriteLine("Enter Matrix 2:")
For i = 0 To 1
For j = 0 To 1
Console.Write("{0}",matrix2(i,j))
Next 
Console.WriteLine()
Next
Console.WriteLine("Multiplication of Matrix 1 and Matrix 2:")
For i = 0 To 1
For j = 0 To 1
sum = 0
For k = 0 To 1
sum += matrix1(i,k) * matrix2(k,j)
Next 
matrix3(i,j) = sum
Next
Next
For i = 0 To 1
For j = 0 To 1
Console.Write("{0}",matrix3(i,j))
Next 
Console.WriteLine()
Next
Console.ReadKey()
End Sub 
End Module

**

