# Proyecto-C-.NET-Escritorio-

using System.ComponentModel.DataAnnotations;

namespace Aplicacion1.Models
{
    public class Usuario
    {
      [key]
      public int Id { get; set; }

      [Required(ErrorMessage = "El Nombre es obligatorio")]

      public string Nombre { get; set; }

      [Required(ErrorMessage = "El Apellido es obligatorio")]

      public string Apellido { get; set; }

      [Required(ErrorMessage = "El Teléfono es Obligatorio")]
      [Display(Name = "Teléfono")]
      public string Telefono { get; set; }
        
      [Required(ErrorMessage = "El correo es Obligatorio")]

      public string Correo { get; set; }
      
      [Required(ErrorMessage = "La dirección es Obligatioria")]

      public string Direccion { get; set; }

     [Required(ErrorMessage = "El cargo es Obligatorio")]

     public string Cargo { get; set; }

     [Required(ErrorMessage = "El salario es Obligatorio")]

     public double Salario { get; set; }

     [Required(ErrorMessage = "La Fecha de Nacimiento es Obligatorio")]

     public double FechaNacimiento { get; set; }

     [Required(ErrorMessage = "El Fecha de Vinculación es Obligatorio")]

     public double FechaVinculacion { get; set; }

     [Required(ErrorMessage = "El Departamento de Trabajo es Obligatorio")]

     public double DepartamentoT { get; set; }

    }
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

{
  "ConnectionStrings": {
    "DefaultConnection": "Server=LAPTOP-AN6VR4QN;Database=CrudUsuario1;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
  
---------------------------------------------------------------------------------------------------------------------------------------------------------------------


builder.Services.AddDbContext<AplicationDBContext>(options =>
    options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection")));
    

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

public class AplicationDBContext : DbContext
    {
        public AplicationDBContext(DbContextOptions<AplicationDBContext>
            options) : base(options)
        {

        }

        public DbSet<Usuario> Usuarios { get; set; }
    }
  
