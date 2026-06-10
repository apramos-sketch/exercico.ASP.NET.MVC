using Microsoft.AspNetCore.Mvc;

namespace MeuProjeto.Controllers
{
    public class HomeController : Controller
    {
        public IActionResult Boletim()
        {
            ViewBag.Disciplinas = new List<string>
            {
                "Matemática", "Português", "História", "Física"
            };

            ViewBag.Notas = new List<double>
           using Microsoft.AspNetCore.Mvc;

namespace MeuProjeto.Controllers
{
    public class ProdutoController : Controller
    {
        public IActionResult Index()
        {
            ViewBag.Produtos = new List<string>
            {
                "Notebook", "Mouse", "Teclado", "Monitor", "Headset"
            };

            ViewBag.Precos = new List<double>
            {
                3500, 80, 150, 900, 95
            };

            return View();
        }
    }
}
@{
    var disciplinas = ViewBag.Disciplinas as List<string>;
    var notas = ViewBag.Notas as List<double>;
    double media = notas.Average();
}

<h2>Boletim</h2>

<table border="1">
<tr>
    <th>Disciplina</th>
    <th>Nota</th>
    <th>Status</th>
    <th>Conceito</th>
</tr>

@for(int i = 0; i < disciplinas.Count; i++)
{
    string conceito = notas[i] >= 9 ? "A" :
                      notas[i] >= 7 ? "B" :
                      notas[i] >= 5 ? "C" : "D";

    <tr>
        <td>@disciplinas[i]</td>
        <td>@notas[i]</td>
        <td style="color:@(notas[i] >= 5 ? "green" : "red")">
            @(notas[i] >= 5 ? "Aprovado" : "Reprovado")
        </td>
        <td>@conceito</td>
    </tr>
}
</table>

<p><strong>Média Geral:</strong> @media</p> {                                                                                                                                         
                9.5, 7.0, 5.5, 4.0
            };

            return View();
        }
    }
    var produtos = ViewBag.Produtos as List<string>;
    var precos = ViewBag.Precos as List<double>;
}

