---
title: Rozúčtování a položky deníku pro faktury dodavatele
description: Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výdaje, daně a náklady zaúčtovány na fakturách dodavatele. Každá částka, která musí být zaúčtována, když je dodavatelská faktura zapsána do deníku, bude mít jedno nebo více rozúčtování.
author: abruer
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 513066a597620450f0b482e98e36d31c6f2c980a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189086"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Rozúčtování a položky deníku pro faktury dodavatele

[!include [banner](../includes/banner.md)]

Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výdaje, daně a náklady zaúčtovány na fakturách dodavatele. Každá částka, která musí být zaúčtována, když je dodavatelská faktura zapsána do deníku, bude mít jedno nebo více rozúčtování. 

## <a name="accounting-distributions"></a>Rozúčtování 

Můžete použít následující tlačítka na stránce Faktura dodavatele pro zobrazení a případnou úpravu rozúčtování pro každou částku na faktuře dodavatele.
-   **Rozúčtovat částky** – zobrazení a úprava rozúčtování pro každý řádek a také všechny podřízené řádky, jako jsou například daně a poplatky. Lze také zobrazit a změnit rozúčtování pro podřízený řádek přímo na stránce Transakcí DPH nebo na stránce Transakce nákladů.
    -   Úprava částek záhlaví faktury dodavatele, například náklady nebo částky zaokrouhlení měny.
    -   Úprava částek řádku faktury dodavatele.
-   **Zobrazit distribuce** – Zobrazení rozúčtování pro všechny řádky v dokumentu. Nelze upravit rozúčtování z tohoto zobrazení.
    -   Zobrazení záhlaví a částek řádku.

Pokud faktura dodavatele odkazuje na nákupní objednávku, můžete rozdělit a změnit rozúčtování pro řádky obsahující zboží, které není na skladě. Pokud řádek faktury dodavatele neobsahuje odkaz na řádek nákupní objednávky, můžete odstranit také rozúčtování. Nelze rozdělit ani odstranit řádky, například na daně, náklady a řádkové slevy. Účet hlavní knihy můžete upravit, ale nelze změnit částky ani procentuální hodnoty.
> [!NOTE]                                                                                                                                 
> Pokud nadřazený řádek obsahuje zboží, které není na skladě a je rozděleno rozúčtování, podřízený řádek bude rozdělen automaticky, aby odpovídal finanční dimenzi nadřazeného řádku. Rozúčtování pro podřízený řádek nelze dále rozdělit ani odstranit, ale v závislosti na nastavení podřízeného řádku je možné upravit účet hlavní knihy pro rozúčtování podřízeného řádku.

## <a name="distributing-amounts"></a>Distribuce částek
Když zadáváte fakturu dodavatele, jednotlivé částky budou rozděleny následujícím způsobem.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ řádku faktury dodavatele</th>
<th>Pořadí priorit, které určuje, odkud se zobrazuje hlavní účet</th>
<th>Pořadí priority, které určuje, jaká výchozí finanční dimenze je zobrazena</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Produkt na skladě</td>
<td><ol>
<li>Rozúčtování řádku nákupní objednávky.</li>
<li>Na stránce Zaúčtování se vybere pole Hlavní účet při výběru Nákupní výdaj pro produkt.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte výchozí hodnoty finanční dimenze na faktuře dodavatele.</li>
</ol></td>
</tr>
<tr class="even">
<td>Kategorie zásobování nebo produkt, který není na skladě</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud faktura dodavatele obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Na stránce Zaúčtování se vybere pole Hlavní účet při výběru Nákupní výdaj pro výdaje.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</li>
<li>Použijte výchozí hodnoty finanční dimenze na faktuře dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Dlouhodobý majetek</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud faktura dodavatele obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Je-li v poli Typ transakce ve formuláři Faktura dodavatele vybráno Pořízení, vybere se také pole Hlavní účet po zvolení Pořízení na stránce Účetní profily dlouhodobého majetku.</li>
<li>Je-li v poli Typ transakce vybrána Oprava pořizovací ceny, vybere se také pole Hlavní účet po zvolení Oprava pořizovací ceny na stránce Účetní profily dlouhodobého majetku.</li>
</ol></td>
<td><ol>
<li>Použijte rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="even">
<td>Projekt definovaný na řádku faktury dodavatele</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Pokud vyberete Zůstatek v poli Zaúčtovat náklady – položka na stránce Skupiny projektů, vybere se pole Hlavní účet po zvolení možnosti Náklady na stránce Nastavení účtování hlavní knihy.</li>
<li>Pokud vyberete Zisk a ztráta v poli Zaúčtovat náklady – položka na stránce Skupiny projektů, vybere se pole Hlavní účet po zvolení možnosti Náklady - položka na stránce Nastavení účtování hlavní knihy.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Řádková sleva</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Pole Hlavní účet při výběru možnosti Sleva na stránce Zaúčtování.</li>
<li>Není-li hlavní účet pro slevu definován v profilu zaúčtování, rozúčtování rozšířené ceny na řádku nákupní objednávky.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze pro řádek faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="even">
<td>Náklady nákupu, které byly zadány na kartě Cena a sleva řádku nákupní objednávky</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Rozúčtování rozšířené ceny na řádku nákupní objednávky.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Náklady na řádek</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Pokud vyberete Účet hlavní knihy v poli Typ ve formuláři Kód nákladů, vybere se pole Účet Má dáti na stránce Kód nákladů.</li>
<li>Pokud je vybrána Položka v poli Typ debetu ve formuláři Kód nákladů, vyberete rozúčtování pro rozšířenou cenu na řádku nákupní objednávky.</li>
<li>Pokud vyberete Odběratel/Dodavatel v poli Typ ve formuláři Kód nákladů, vybere se pole Účet Dal na stránce Kód nákladů.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="even">
<td>Daň s následující podmínkou:
<ul>
<li>Na stránce Parametry hlavní knihy je zaškrtnuto políčko Použít daňové předpisy platné v USA.</li>
</ul></td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Rozúčtování rozšířené ceny nebo nákladů.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Daň s následujícími podmínkami:
<ul>
<li>Na stránce Parametry hlavní knihy je zrušeno označení políčka Použít daňové předpisy platné v USA.</li>
<li>Na stránce Skupiny prodejní daně je pro skupinu DPH zrušeno označení pole Importní DPH.</li>
</ul></td>
<td><ol>
<li>Pokud je částka DPH vratná, vybere se pole DPH na vstupu na stránce Účetní skupiny.</li>
<li>Pokud není částka daně vratná, rozšířená cena nebo rozúčtování pro náklady.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozšířené ceny nebo rozúčtování pro náklady na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="even">
<td>Daň s následujícími podmínkami:
<ul>
<li>Na stránce Parametry hlavní knihy je zrušeno označení políčka Použít daňové předpisy platné v USA.</li>
<li>Na stránce Skupiny prodejní daně je pro skupinu DPH vybráno pole Importní DPH.</li>
</ul></td>
<td><ol>
<li>Pokud je částka DPH vratná, vybere se pole DPH na vstupu na stránce Účetní skupiny.</li>
<li>Pokud částka DPH není vratná, vybere se pole Importní DPH – výdaj na stránce Účetní skupiny.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozšířené ceny nebo rozúčtování pro náklady na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Náklady v záhlaví</td>
<td><ol>
<li>Pokud vyberete Účet hlavní knihy v poli Typ ve formuláři Kód nákladů, vybere se pole Účet Má dáti na stránce Kód nákladů.</li>
<li>Pokud vyberete Odběratel/Dodavatel v poli Typ ve formuláři Kód nákladů, vybere se pole Účet Dal na stránce Kód nákladů.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</li>
<li>Použijte hodnoty výchozí šablony finanční dimenze ze záhlaví faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
<tr class="even">
<td>Sleva záhlaví</td>
<td><ol>
<li>Pole Hlavní účet pro typ zaúčtování Sleva faktury dodavatele na stránce Účty pro automatické transakce.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Distribuce daní

Dokud daně nejsou vypočítány, nelze pro ně vytvořit rozúčtování. Při výpočtu DPH je třeba na stránce Faktura dodavatele provést jeden z následujících úkolů:
-   Zobrazit celkový součet faktury.
-   Zobrazit DPH.
-   Zobrazit dílčí hlavní knihu.
-   Zobrazit rozúčtování pro kompletní fakturu dodavatele.
-   Blokovat fakturu dodavatele.
-   Zaúčtovat fakturu dodavatele.

## <a name="subledger-journals-for-vendor-invoices"></a>Dílčí hlavní deníky pro faktury dodavatele
Před zaúčtováním faktury dodavatele můžete zobrazit celý účetní zápis faktury, který zahrnuje pohledávky a závazky, abyste ověřili, zda je faktura zaúčtována na správné účty. Toto zobrazení celkového zápisu do účetnictví se nazývá dílčí hlavní kniha. 

Pokud není položka dílčí hlavní knihy správná při zobrazení náhledu než zapíšete fakturu dodavatele do deníku, položku dílčí hlavní knihy nelze změnit. Namísto toho je nutné upravit rozúčtování nebo účetní profil. Rozúčtování slouží k definování jedné strany účetní položky, má dáti nebo dal. Vyrovnání účetní položky dílčí hlavní knihy je vytvořeno pomocí účetních profilů, jako je například účet dodavatele nebo daň.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]