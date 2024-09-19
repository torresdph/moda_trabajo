# moda_trabajo
trabajo de moda
<?php
session_start();
if (!isset($_SESSION['user'])) {
    header("Location: login.php");
    exit;
}

include 'app/Conect.php'; // Incluir archivo de conexión
include 'app/Acciones.php'; // Incluir archivo de acciones

$acciones = new Acciones($Conecta); // Crear instancia de Acciones
$moda = $acciones->mostrarModa(); // Obtener los artículos de moda
?>
