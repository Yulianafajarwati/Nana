<?php 
// membuat class biodata
 class Biodata{
 	// menyimpan data dalam array
 	public $data = [];
 	// fungsi nama
 	public function nama($nama)
 	{
 		$this->data['name'] = $nama;
 		return $this;
 	}
 	// fungsi umur
 	public function umur($umur)
 	{
 	    $this->data['age'] = $umur;
 	    return $this;
 	}
 	// fungsi alamat
 	public function alamat($alamat)
 	{
 		$this->data['address'] = $alamat;
 		return $this;
 	}
 	// fungsi hobi
 	public function hobi($hobi = array())
 	{
 		$this->data['hobbies'] = $hobi;
 		return $this;
 	}
 	
 	// fungsi menikah
 	public function menikah($menikah)
 	{
 		$this->data['is_married'] = $menikah;
 		return $this;
 	}
 	
 	// fungsi sekolah
 	public function sekolah($sekolah = array())
 	{
 		$this->data['school'] = $sekolah;
 		return $this;
 	}
 	// fungsi kemampuan
 	public function kemampuan($kemampuan = array())
 	{
 		$this->data['skills'] = $kemampuan;
 		return $this;
 	}
 	// fungsi konvert ke json
 	public function konjson(){
 		return json_encode($this->data, JSON_PRETTY_PRINT);
 	}
 	
}
$biodata 	= new Biodata();
$nama		= "YULIANA FAJARWATI";
$umur       = 22;
$alamat		= ['Jalan Al latif RT 05 RW 07. Cijantung. Jakarta Timur'];
$hobi 		= ['Membaca','jalan-jalan','Ngoding'];
$sekolah	= [
				"highSchool" 	=> "SMAN 1 KALITIDU",
				"university" 	=> "UNIVERSITAS GUNADARMA"
			  ];
$kemampuan	= [
				"Web"		=> ['PHP','CSS','HTML'],
				"Olahraga"	=> ['Sepedah, Bulu Tangkis']
			  ];
print_r($biodata->nama($nama)
                ->umur($umur)
				->alamat($alamat)
				->hobi($hobi)
				->menikah(false)
				->sekolah($sekolah)
				->kemampuan($kemampuan)
				->konjson()
);
