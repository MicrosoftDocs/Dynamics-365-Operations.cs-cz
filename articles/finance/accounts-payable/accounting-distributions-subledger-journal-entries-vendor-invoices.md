---
title: Rozúčtování a položky deníku pro faktury dodavatele
description: Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výdaje, daně a náklady zaúčtovány na fakturách dodavatele. Každá částka, která musí být zaúčtována, když je dodavatelská faktura zapsána do deníku, bude mít jedno nebo více rozúčtování.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358174"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Rozúčtování a položky deníku pro faktury dodavatele

[!include [banner](../includes/banner.md)]

Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výdaje, daně a náklady zaúčtovány na fakturách dodavatele. Každá částka, která musí být zaúčtována, když je dodavatelská faktura zapsána do deníku, bude mít jedno nebo více rozúčtování. 

## <a name="accounting-distributions"></a>Rozúčtování 

Můžete použít následující tlačítka na stránce Faktura dodavatele pro zobrazení a případnou úpravu rozúčtování pro každou částku na faktuře dodavatele.
-   **Rozúčtovat částky** – zobrazení a úprava rozúčtování pro každý řádek a také všechny podřízené řádky, jako jsou například daně a poplatky. Lze také zobrazit a změnit rozúčtování pro podřízený řádek přímo na stránce **Transakce DPH** nebo na stránce **Transakce nákladů**.
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
<li>Na stránce <strong>Zaúčtování</strong> se vybere pole <strong>Hlavní účet</strong> při výběru Nákupní výdaj pro produkt.</li>
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
<li>Na stránce <strong>Zaúčtování</strong> se vybere pole <strong>Hlavní účet</strong> při výběru Nákupní výdaj pro výdaje.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</li>
<li>Použijte výchozí hodnoty finanční dimenze na faktuře dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce <strong>Účtová osnova</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Dlouhodobý majetek</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud faktura dodavatele obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Je-li v poli <strong>Typ transakce</strong> na stránce <strong>Faktura dodavatele</strong> vybráno <strong>Pořízení</strong>, vybere se také pole <strong>Hlavní účet</strong> po zvolení <strong>Pořízení</strong> na stránce <strong>Účetní profily dlouhodobého majetku</strong>.</li>
<li>Je-li v poli <strong>Typ transakce</strong> vybrána <strong>Oprava pořizovací ceny</strong>, vybere se také pole <strong>Hlavní účet</strong> po zvolení možnosti <strong>Oprava pořizovací ceny</strong> na stránce <strong>Účetní profily dlouhodobého majetku</strong>.</li>
</ol></td>
<td><ol>
<li>Použijte rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce <strong>Účtová osnova</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Projekt definovaný na řádku faktury dodavatele</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Pokud vyberete <strong>Zůstatek</strong> v poli <strong>Zaúčtovat náklady – položka</strong> na stránce <strong>Skupiny projektů</strong>, vybere se pole <strong>Hlavní účet</strong> po zvolení možnosti <strong>Náklady</strong> na stránce <strong>Nastavení účtování hlavní knihy</strong>.</li>
<li>Pokud vyberete <strong>Zisk a ztráta</strong> v poli <strong>Zaúčtovat náklady – položka</strong> na stránce <strong>Skupiny projektů</strong>, vybere se pole <strong>Hlavní účet</strong> po zvolení možnosti <strong>Náklady - položka</strong> na stránce <strong>Nastavení účtování hlavní knihy</strong>.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Řádková sleva</td>
<td><ol>
<li>Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</li>
<li>Pole <strong>Hlavní účet</strong> při výběru možnosti <strong>Sleva</strong> na stránce <strong>Zaúčtování</strong>.</li>
<li>Není-li hlavní účet pro slevu definován v profilu zaúčtování, rozúčtování rozšířené ceny na řádku nákupní objednávky.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze pro řádek faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce <strong>Účtová osnova</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Náklady nákupu, které byly zadány na kartě <strong>Cena a sleva</strong> řádku nákupní objednávky</td>
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
<li>Pokud vyberete <strong>Účet hlavní knihy</strong> v poli <strong>Typ debetu</strong> na stránce <strong>Kód nákladů</strong>, vybere se pole <strong>MD účet</strong> na stránce <strong>Kód nákladů</strong>.</li>
<li>Pokud je vybrána <strong>Položka</strong> v poli <strong>Typ debetu</strong> na stránce <strong>Kód nákladů</strong>, vyberete rozúčtování pro rozšířenou cenu na řádku nákupní objednávky.</li>
<li>Pokud vyberete <strong>Odběratel/Dodavatel</strong> v poli <strong>Typ debetu</strong> na stránce <strong>Kód nákladů</strong>, vybere se pole <strong>Dal účet</strong> na stránce <strong>Kód nákladů</strong>.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce <strong>Účtová osnova</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Daň s následující podmínkou:
<ul>
<li>Na stránce <strong>Parametry hlavní knihy</strong> je zaškrtnuto políčko <strong>Použít daňové předpisy platné v USA</strong>.</li>
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
<li>Na stránce <strong>Parametry hlavní knihy</strong> je vypnuto políčko <strong>Použít daňové předpisy platné v USA</strong>.</li>
<li>Na stránce <strong>Skupiny prodejní daně</strong> je pro skupinu DPH zrušeno označení pole <strong>Importní DPH</strong>.</li>
</ul></td>
<td><ol>
<li>Pokud je částka DPH vratná, vybere se pole <strong>DPH</strong> na vstupu na stránce <strong>Účetní skupiny</strong>.</li>
<li>Pokud není částka daně vratná, rozšířená cena nebo rozúčtování pro náklady.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozšířené ceny nebo rozúčtování pro náklady na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce <strong>Účtová osnova</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Daň s následujícími podmínkami:
<ul>
<li>Na stránce <strong>Parametry hlavní knihy</strong> je zrušeno označení políčka Použít daňové předpisy platné v USA.</li>
<li>Na stránce <strong>Skupiny prodejní daně</strong> je pro skupinu DPH vybráno pole <strong>Importní DPH</strong>.</li>
</ul></td>
<td><ol>
<li>Pokud je částka DPH vratná, vybere se pole <strong>DPH</strong> na vstupu na stránce <strong>Účetní skupiny</strong>.</li>
<li>Pokud částka DPH není vratná, vybere se pole <strong>Importní DPH – výdaj</strong> na stránce <strong>Účetní skupiny</strong>.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozšířené ceny nebo rozúčtování pro náklady na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce <strong>Účtová osnova</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Náklady v záhlaví</td>
<td><ol>
<li>Pokud vyberete <strong>Účet hlavní knihy</strong> v poli <strong>Typ debetu</strong> na stránce <strong>Kód nákladů</strong>, vybere se pole <strong>MD účet</strong> na stránce <strong>Kód nákladů</strong>.</li>
<li>Pokud vyberete <strong>Odběratel/Dodavatel</strong> v poli <strong>Typ debetu</strong> na stránce <strong>Kód nákladů</strong>, vybere se pole <strong>Dal účet</strong> na stránce <strong>Kód nákladů</strong>.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</li>
<li>Použijte hodnoty výchozí šablony finanční dimenze ze záhlaví faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce <strong>Účtová osnova</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Sleva záhlaví</td>
<td><ol>
<li>Pole <strong>Hlavní účet</strong> pro <strong>typ zaúčtování Sleva faktury dodavatele</strong> na stránce <strong>Účty pro automatické transakce</strong>.</li>
</ol></td>
<td><ol>
<li>Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</li>
<li>Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</li>
<li>Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</li>
<li>Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce <strong>Účtová osnova</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Distribuce daní

Dokud daně nejsou vypočítány, nelze pro ně vytvořit rozúčtování. Při výpočtu DPH je třeba na stránce **Faktura dodavatele** provést jeden z následujících úkolů:
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
