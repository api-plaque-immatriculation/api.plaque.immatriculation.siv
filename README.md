# API Plaque Immatriculation France

Cette API permet de récupérer des informations détaillées sur un véhicule à partir de sa plaque d'immatriculation française.

## Utilisation

### Requête API

Pour interroger l'API, vous devez envoyer une requête POST avec les paramètres suivants :

- `immatriculation` : La plaque d'immatriculation du véhicule (ex: `AA-123-BC`).
- `token` : Votre token d'authentification (ex: `TokenDemo2025`).
- `pays` : Le pays de la plaque d'immatriculation (ex: `FR` pour la France).

### Exemple de requête en PHP

```php
<?php
$curl = curl_init();
curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://api.apiplaqueimmatriculation.com/get-vehicule-info?immatriculation=AA-123-BC&token=TokenDemo2025&pays=FR',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST'
));
$response = curl_exec($curl);
curl_close($curl);
echo $response;
?>

Réponse de l'API
La réponse de l'API est au format JSON et contient les informations suivantes :


{
  "data": {
    "erreur": "",
    "immat": "AA123BC",
    "pays": "FR",
    "marque": "RENAULT",
    "modele": "MEGANE III",
    "date1erCir_us": "2009-04-18",
    "date1erCir_fr": "18-04-2009",
    "co2": "134",
    "energie": "2",
    "energieNGC": "DIESEL",
    "genreVCG": "1",
    "genreVCGNGC": "VP",
    "puisFisc": "7",
    "carrosserieCG": "COUPE",
    "puisFiscReelKW": "96 KW",
    "puisFiscReelCH": "131 CH",
    "collection": "non",
    "date30": "1989-06-30",
    "vin": "VF1DZ0N0641118804",
    "variante": "DZ0N06",
    "boite_vitesse": "M",
    "code_boite_vitesse": "",
    "nr_passagers": "5",
    "nb_portes": "5",
    "type_mine": "",
    "cnit": "",
    "couleur": "NOIR",
    "poids": "1807 kg",
    "ccm": "1870 CM3",
    "cylindres": "4",
    "sra_id": "RE80126",
    "sra_group": "32",
    "sra_commercial": "1.9 DCI 130 XV DE FRANCE",
    "numero_serie": "41118804",
    "ptac": "",
    "logo_marque": "https://api.apiplaqueimmatriculation.com/public/storage/logos_marques/?marque=renault",
    "k_type": "31164",
    "tecdoc_manuid": "0",
    "tecdoc_modelid": "0",
    "tecdoc_carid": "31164",
    "code_moteur": "F9Q(870|872)",
    "codes_platforme": "DZ0/1_"
  },
  "api-version": "1.0.0"
}
