          # 03.10.2023_
          Андреев
          Хабибуллина
          ИП-11
          using System;
          using System.Collections.Generic;
          using System.Linq;
          using System.Text;
          using System.Threading.Tasks;
          
          namespace StringReverseLibrary
          {
              public class StringReversClass
              {
                  /// <summary>
                  /// В качестве параметра передается строка, представляющая одно слово и содержащая ноль или более символов.
                  /// </summary>
                  /// <param name="textString"></param>
                  /// Возвращается “перевернутая” строка, в которой последний символ станет первым, предпоследний вторым и т. д. Все символы возвращаются в нижнем регистре
                  /// <returns></returns>
                  /// <exception cref="Exception"></exception>
                  public static string ReverseString(string textString)
                  {
                      char[] chars = textString.ToCharArray();
                      Array.Reverse(chars);
                      if (textString == null)
                      {
                          throw new Exception("Пустота");
                      }
                      return new string(chars).ToLower();
                  }
              }
          }




            
                      using Microsoft.VisualStudio.TestTools.UnitTesting;
            using StringReverseLibrary;
            using System;
            using System.Collections.Generic;
            using System.Linq;
            using System.Text;
            using System.Threading.Tasks;
            
            namespace StringReverseLibrary.Tests
            {
                [TestClass()]
                public class Revers
                {
                    [TestMethod()]
                    public void Reverse_1()
                    {
                        //Arrange
                        string textString = "Привет!";
                        //Act
                        string expected = "!тевирп";
                        string actual = StringReversClass.ReverseString(textString);
                        //Assert
                        Assert.AreEqual(expected, actual);
                    }
                    [TestMethod]
                    public void Revers_Exeption()
                    {
                        //Arrange
                        string textString = "";
                        //Act
                        Action actual = () => StringReversClass.ReverseString(textString);
                        //Assert
                        Assert.ThrowsException<Exception>(actual);
                    }
                    [TestMethod]
                    public void Revers_2()
                    {
                        //Arrange
                        string textString = "qwerty";
                        //Act
                        string expected = "ytrewq";
                        string actual = StringReversClass.ReverseString(textString);
                        //Assert
                        Assert.AreEqual(expected, actual);
                    }
                    [TestMethod]
            
                    public void Rever_3()
                    {
                        //Arrange
                        string textString = "Qwerty";
                        //Act
                        string expected = "ytrewq";
                        string actual = StringReversClass.ReverseString(textString);
                        //Assert
                        Assert.AreEqual(expected, actual);
                    }
            
                }
            }





          
