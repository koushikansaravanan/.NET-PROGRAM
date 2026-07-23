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

**calculator**

Public Class Form1
    Dim fr As Double ' First value
    Dim sv As Double ' Second value
    Dim ans As Double ' Result
    Dim sy As String ' Operator  


    Private Sub Button14_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button14.Click
        TextBox1.Text &= "1"
    End Sub

    Private Sub Button15_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button15.Click
        TextBox1.Text &= "2"
    End Sub

    Private Sub Button16_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button16.Click
        TextBox1.Text &= "3"
    End Sub

    Private Sub Button7_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button7.Click
        TextBox1.Text &= "4"
    End Sub

    Private Sub Button6_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button6.Click
        TextBox1.Text &= "5"
    End Sub

    Private Sub Button5_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button5.Click
        TextBox1.Text &= "6"
    End Sub

    Private Sub Button3_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button3.Click
        TextBox1.Text &= "7"
    End Sub

    Private Sub Button2_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button2.Click
        TextBox1.Text &= "8"
    End Sub

    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click
        TextBox1.Text &= "9"
    End Sub

    Private Sub Button12_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button12.Click
        TextBox1.Clear()
        fr = 0
        sv = 0
        sy = ""
    End Sub

    Private Sub Button9_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button9.Click
        sv = Val(TextBox1.Text)
        Select Case sy
            Case "+"
                ans = fr + sv
            Case "-"
                ans = fr - sv
            Case "*"
                ans = fr * sv
            Case "/"
                If sv = 0 Then
                    MessageBox.Show("Cannot divide by zero")
                    Exit Sub
                End If
                ans = fr / sv
        End Select
        TextBox1.Text = ans.ToString()
    End Sub

    Private Sub Button4_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button4.Click
        fr = Val(TextBox1.Text)
        TextBox1.Clear()
        sy = "+"
    End Sub

    Private Sub Button8_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button8.Click
        fr = Val(TextBox1.Text)
        TextBox1.Clear()
        sy = "-"
    End Sub

    Private Sub Button13_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button13.Click
        fr = Val(TextBox1.Text)
        TextBox1.Clear()
        sy = "*"
    End Sub

    Private Sub Button10_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button10.Click
        fr = Val(TextBox1.Text)
        TextBox1.Clear()
        sy = "/"
    End Sub

    Private Sub Button11_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button11.Click
        TextBox1.Text &= "0"
    End Sub
End Class


