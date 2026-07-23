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


**digital clock**

Public Class Form1

    Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load
        Label3.Text = "digital clock"
        Label1.Text = "00:00:00"
        Label3.Text = "00-00.0000"
    End Sub


    Private Sub Timer1_Tick(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Timer1.Tick
        Label1.Text = TimeString '12 hours timw
        Label1.Text = DateTime.Now.ToString("hh:mm:ss tt")
        Label2.Text = DateTime.Now.ToString("dd-MM-yyyy")
    End Sub

    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click
        Timer1.Start()
    End Sub

    Private Sub Button2_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button2.Click
        Timer1.Stop()
        Label1.Text = "00:00:0"
    End Sub

    Private Sub Button3_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button3.Click
        Timer1.Stop()
    End Sub
End Class


**employee account**

Public Class Form1
    Dim eid() As Integer = {101, 102, 103}
    Dim ename() As String = {"Ravi", "Priya", "Arun"}
    Dim basic() As Integer = {20000, 25000, 30000}
    Dim hra() As Integer = {5000, 6000, 7000}
    Dim index As Integer = 0
    Private Sub DisplayData()
        txtEID.Text = eid(index)
        txtName.Text = ename(index)
        txtBasic.Text = basic(index)
        txtHRA.Text = hra(index)
        txtNet.Text = basic(index) + hra(index)
    End Sub
    Private Sub Form1_Load(ByVal sender As Object, ByVal e As EventArgs) Handles MyBase.Load
        DisplayData()
    End Sub

    Private Sub btnFirst_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnFirst.Click
        index = 0
        DisplayData()
    End Sub

    Private Sub btnLast_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnLast.Click
         index = eid.Length - 1
        DisplayData()
    End Sub

    Private Sub btnNext_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnNext.Click
        If index < eid.Length - 1 Then
            index += 1
            DisplayData()
        End If
    End Sub

    Private Sub btnPrevious_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnPrevious.Click
        If index > 0 Then
            index -= 1
            DisplayData()
        End If
    End Sub
End Class



