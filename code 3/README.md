Nama : Adli Asirof

Kls : D4 Teknik Informatika 3B

Npm : 1144069

Barang.xml

| \<?xmlversion="1.0"encoding="UTF-8"?\>\<logbarangxmlns:xsd=\_"http://www.w3.org/2001/XMLSchema\&quot;\_xmlns:xsi=\_&quot;http://www.w3.org/2001/XMLSchema-instance&quot;\_xsi:noNamespaceSchemaLocation=\_&quot;barang.xsd&quot;\_&gt;&lt;barang&gt;&lt;kode&gt;M1112&lt;/kode&gt;&lt;satuan&gt;pc&lt;/satuan&gt;&lt;harga&gt;5000&lt;/harga&gt;&lt;asal&gt;&lt;pt&gt;ladyrock&lt;/pt&gt;&lt;kodewil&gt;10&lt;/kodewil&gt;&lt;/asal&gt;&lt;tujuan&gt;&lt;pt&gt;union&lt;/pt&gt;&lt;kodewil&gt;1000&lt;/kodewil&gt;&lt;/tujuan&gt;&lt;/barang&gt;&lt;barang&gt;&lt;kode&gt;M1122&lt;/kode&gt;&lt;satuan&gt;pc&lt;/satuan&gt;&lt;harga&gt;1001&lt;/harga&gt;&lt;asal&gt;&lt;pt&gt;pbm&lt;/pt&gt;&lt;kodewil&gt;103&lt;/kodewil&gt;&lt;/asal&gt;&lt;tujuan&gt;&lt;pt&gt;mitrakencana&lt;/pt&gt;&lt;kodewil&gt;300&lt;/kodewil&gt;&lt;/tujuan&gt;&lt;/barang&gt;&lt;/logbarang\> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|


Barang.xsd

| \<xs:schemaxmlns:xs="http://www.w3.org/2001/XMLSchema\&quot;\_elementFormDefault=\_&quot;qualified"\> \<xs:elementname="logbarang"\> \<xs:complexType\> \<xs:sequence\> \<xs:elementmaxOccurs="unbounded"ref="barang"minOccurs="1"/\> \</xs:sequence\> \</xs:complexType\> \</xs:element\> \<xs:elementname="barang"\> \<xs:complexType\> \<xs:sequence\> \<xs:elementref="kode"minOccurs="1"/\> \<xs:elementref="satuan"/\> \<xs:elementref="harga"/\> \<xs:elementref="asal"/\> \<xs:elementref="tujuan"/\> \</xs:sequence\> \</xs:complexType\> \</xs:element\> \<xs:elementname="kode"\> \<xs:simpleType\> \<xs:restrictionbase="xs:string"\> \<xs:minLengthvalue="5"\>\</xs:minLength\> \<xs:patternvalue="[A-Z]+.+"\>\</xs:pattern\> \</xs:restriction\> \</xs:simpleType\> \</xs:element\> \<xs:elementname="satuan"type="xs:NCName"/\> \<xs:elementname="harga"\> \<xs:simpleType\> \<xs:restrictionbase="xs:integer"\> \<xs:minExclusivevalue="1000"\>\</xs:minExclusive\> \</xs:restriction\> \</xs:simpleType\> \</xs:element\> \<xs:elementname="asal"\> \<xs:complexType\> \<xs:sequence\> \<xs:elementref="pt"/\> \<xs:elementref="kodewil"/\> \</xs:sequence\> \</xs:complexType\> \</xs:element\> \<xs:elementname="tujuan"\> \<xs:complexType\> \<xs:sequence\> \<xs:elementref="pt"/\> \<xs:elementref="kodewil"/\> \</xs:sequence\> \</xs:complexType\> \</xs:element\> \<xs:elementname="pt"type="xs:string"/\> \<xs:elementname="kodewil"type="xs:integer"/\>\</xs:schema\> |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|


Analisa :

XSD bisa dingunakan sebagai pembatasan dalam sebuah xml.

| \<xs:elementname="kode"\> \<xs:simpleType\> \<xs:restrictionbase="xs:string"\> \<xs:minLengthvalue="5"\>\</xs:minLength\> \<xs:patternvalue="[A-Z]+.+"\>\</xs:pattern\> \</xs:restriction\> \</xs:simpleType\> \</xs:element\> |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|


Pada element kode dengan type yang digunakan adalah string memiliki minimal
lebar 5 dengan pattern value menggunakan huruf / karakter yang harus berhuruf
besar dan tidak boleh tidak diisi, jika value kosong maka akan error.

| \<xs:elementname="harga"\> \<xs:simpleType\> \<xs:restrictionbase="xs:integer"\> \<xs:minExclusivevalue="1000"\>\</xs:minExclusive\> \</xs:restriction\> \</xs:simpleType\> \</xs:element\> |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|


Pada element harga dengan type data integer memiliki batasa dimana value dalam
element harus lebih dari 1000, jika kurang maka akan terjadi error.
