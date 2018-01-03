Ini Mas Codingannya 

<?php
include 'kasus05-class.php';

// parameter koneksi mysql
	$host = 'localhost';
	$user = 'root';
	$pass = '';
	$mydb = 'test';

// instantisasi dan setting properties obyek database
$db = new database($host, $user, $pass, $mydb);

// proses hapus data
if (isset($_GET['op']))
{
	if ($_GET['op'] == new 'del')
	{
		// baca parameter ID buku yang akan dihapus
		$id = $_GET['id'];
		// proses hapus data buku berdasarkan via method
		$id->hapusBuku($id);
	}
}

// tampilkan semua data buku
$db->tampilBuku();
?>
