---
title: Nastavení účtů dodavatele
description: Toto téma popisuje typy informací, které je nutné zadat při vytváření nového účtu dodavatele.
author: mkirknel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63843381207fbe6cb72ac1b5533eda754b1ba55b
ms.sourcegitcommit: 5457cbec3399d8ed9f87c3a9dc586173b5616c11
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3012438"
---
# <a name="set-up-vendor-accounts"></a>Nastavení účtů dodavatele

[!include [banner](../includes/banner.md)]

Toto téma popisuje typy informací, které je nutné zadat při vytváření nového účtu dodavatele.

Při vytvoření účtu dodavatele zadáváte informace o dodavateli. Tyto informace slouží k automatickému zadání dat do dokumentů a ke sledování aktivity, která zahrnuje dodavatele. Můžete například konfigurovat následující informace o dodavateli:

-   Přiřadit skupinu dodavatelů. Každý dodavatel musí být přiřazen ke skupině dodavatelů. Dodavatelé ve skupině dodavatelů mají parametry, které sdílejí. Například mohou mít stejné platební podmínky.
-   Konfigurujte dodavatele pro import katalogu. Dodavatelé mohou poskytnout soubor, který obsahuje katalog jejich položek a služeb. Tento soubor lze odeslat, aby tak vaši pracovníci mohli objednávat od tohoto dodavatele.
-   Přiřadit dodavatele ke kategoriím zásobování.
-   Povolit existujícímu dodavateli obchodovat s jiným právním subjektem v organizaci.
-   Pro konkrétní typy transakcí lze dodavatele blokovat.
-   Nastavit bankovní informace pro dodavatele, aby bylo možné platby odesílat elektronicky.
-   Nastavit daňové, dodací, fakturační a platební údaje dodavatele. Ve výchozím nastavení jsou tyto údaje zkopírovány do nových dokumentů, které pro dodavatele vytvoříte.
-   Nastavit výchozí finanční dimenze používané k automatickému zaúčtování transakcí s dodavatelem na finanční účty.

Chcete-li urychlit proces vytváření účtů dodavatelů, můžete vytvořit šablony. K vytvoření šablony na stránce **Dodavatel** v podokně akcí klikněte na **Možnost** &gt; **Informace o záznamu**. Dále klikněte na **Šablona účtů společnosti**. Šablony účtů společnosti jsou sdíleny s ostatními uživateli.  

Můžete také vytvořit šablonu uživatele pro vaši vlastní potřebu. Nelze odstranit dodavatele přidruženého k dalším záznamům, jako jsou například kontakty nebo produkty.

## <a name="vendor-account-numbers"></a>Čísla účtu dodavatele
Číslo účtu je jedinečný identifikátor dodavatele. Čísla účtů můžete vytvořit tak, aby byla automaticky generována při vytvoření dodavatele. Můžete také nastavit číselnou řadu a čísla účtů tak zadávat ručně. Například můžete chtít jako identifikátor použít telefonní číslo dodavatele.

## <a name="vendor-organizations-and-individual-vendors"></a>Organizace dodavatele a jednotliví dodavatelé
Když vytvoříte nový účet dodavatele, je nutné vybrat, zda je dodavatel organizací nebo jednotlivcem. Výběr ovlivňuje informace, které je nutné pro dodavatele vyplnit. U jednotlivce tyto informace zahrnují jméno, příjmení a titul. V případě organizace tyto informace zahrnují číslo organizace a počet zaměstnanců.

## <a name="addresses"></a>Adresy
Pro každého dodavatele lze definovat více adres, kde se každá z nich používá pro různé účely. Lze například vytvořit adresu, která má účel **Faktura**. Nebo chcete-li vyplatit dodavatele pomocí šeků, můžete vytvořit adresu s účelem **Uhradit**. Pokud je nutné zadat adresu, kterou chcete použít pro peněžní převody do zahraničních bank, účel bude **SWIFT**.

## <a name="vendor-contacts"></a>Kontakty dodavatele
U dodavatelů lze uložit kontakty. Tyto kontakty lze použít v dokumentech, jako jsou například nákupní objednávky nebo požadavky na nabídku.  

Pokud budete chtít přidat kontakty k dodavateli, na stránce **Všichni dodavatelé** na kartě **Dodavatel** klikněte ve skupině **Nastavení** na tlačítko **Kontakty** &gt; **Přidat kontakty**.  

Kontakty dodavatelů můžete vytvářet zcela od začátku. Také můžete zkopírovat informace od jiného uživatele, který je již registrován v aplikaci Supply Chain Management, a informace podle potřeby upravit.  

**Poznámka:** přidáním kontaktu k dodavateli není to stejné, jako přidání kontaktních údajů k danému dodavateli. Ačkoli jste mohli u dodavatele přidat obecné kontaktní údaje, mohou existovat další konkrétní osoby, které působí jako kontakty v dané společnosti, které mají své vlastní kontaktní údaje.  

Záznam kontaktní osoby nelze odstranit, pokud je na tento kontakt v dokumentu odkazováno. Namísto toho lze kontakt deaktivovat.  

Kontakty dodavatele můžete přidat do osobních kontaktů ve službách Microsoft Office 365. Nejprve je však nutné nastavit synchronizaci mezi aplikací Supply Chain Management a službami Office 365 v rámci synchronizace serveru Microsoft Exchange Server a průvodci instalací pro aplikaci Microsoft Outlook.

## <a name="vendors-in-different-legal-entities"></a>Dodavatelé z různých právnických osob
Dodavatel je ve vaší organizaci registrován pouze pro jednu právnickou osobu a ostatní právnické osoby si musí zaregistrovat stejného dodavatele. Ke konfiguraci dodavatele pro jinou právnickou osobu lze použít stránku **Přidat dodavatele k jiné právnické osobě**. U dodavatele je ve vybrané právnické osobě nutné určit skupinu dodavatelů, měnu a stav blokování.  

Pokud s jedním dodavatelem obchoduje více právnických osob ve vaší organizaci a každá právnická osoba používá pro daného dodavatele oddělený účet dodavatele, použijte následující postup ke sloučení ID strany pro účty dodavatele. V takovém případě lze informace, jako například adresu a počet zaměstnanců, sdílet, což vám umožní údaje aktualizovat pouze na jednom místě.  

Ke sloučení ID strany postupujte takto.

1.  Na stránce **Globální adresář** vyberte záznamy adresáře, které reprezentují dodavatele v jednotlivých právnických osobách, které mají být zahrnuty do mapování.
2.  V podokně akcí klepněte na **Sloučit záznamy**.

## <a name="agreements"></a>Smlouvy
Když vytváříte účet dodavatele, můžete také zaregistrovat smlouvy, které máte s dodavatelem. Pomocí akcí v záznamu dodavatele lze nastavit smlouvy o cenách a slevách. Na stránce **Nákupní smlouvy** lze nastavit nákupní smlouvu.

## <a name="putting-a-vendor-on-hold"></a>Blokování dodavatele
Dodavatele je možné blokovat pro různé typy transakcí. Existují tyto možnosti:

-   **Ne** – dodavatel není nijak blokován.
-   **Faktura** – pro dodavatele nelze zaúčtovat žádné faktury.
-   **Vše** – dodavatel je blokován pro všechny typy transakcí. Tyto typy transakcí zahrnují nákupní požadavky, faktury a platby.
-   **Platba** – žádné platby nemohou být pro dodavatele generovány.
-   **Žádanka** – nelze vytvořit nákupní žádanky pro dodavatele a řádky žádanky, které byly vytvořeny před nastavením dodavatele pro blokování, nelze převést na nákupní objednávku. Řádky požadavků pro dodavatele budou zrušeny, pokud jsou nastaveny zásady pro automatické vytváření nákupních objednávek.
-   **Nikdy** – dodavatele nebude nikdy blokován pro nečinnost.

Pokud dodavatele budete blokovat, můžete také nastavit důvod a datum, kdy stav blokování skončí. Pokud nezadáte datum ukončení, blokování dodavatele bude trvat navždy.

Můžete hromadně aktualizovat blokování všech **Všichni** dodavatelů na základě zvolených kritérií na stránce **Deaktivace dodavatele** a přiřadit důvod blokace dodavatele.

Následující kritéria jsou použity pro zařazení dodavatele, který byl po nějakou dobu neaktivní, zařadit nebo vyřadit dodavatele, kteří jsou zároveň zaměstnanci, a vyřadit dodavatele, kteří jsou v přechodném obdobím před dalším vyřazením.

- Na základě počtu dní, které vložíte do pole **Aktivní období** na stránce **Deaktivace dodavatele**, aplikace spočítá poslední datum, kdy může dodavatel provést jakoukoliv činnost, aby byl považován za neaktivního. To je aktuální datum minus počet dnů, které jste vložili. Pokud pro daného dodavatele existuje jedna nebo více faktur, u kterých je datum splatnosti pozdější než vypočítané poslední datum, dodavatel bude z deaktivace vyřazen. Toto platí i v případě, že dodavatel má platby po daném datu, otevřené nákupní žádanky, otevřené nákupní příkazy, žádosti o cenovou nabídku nebo odpovědi.
- Počet dní v poli **Přechodné období před dalším blokováním** se použije pro výpočet posledního dne přechodného období. To znamená aktuální datum minus počet dnů, které jste vložili. Toto se týká pouze dodavatelů, kteří již byli v minulosti deaktivováni. V případě předchozí deaktivace aplikace ověří historii dalších výskytů deaktivace dodavatele a zkontroluje, zda poslední deaktivace nastala před posledním dnem přechodného období. Pokud ano, dodavatel bude zařazen v procesu deaktivace.
- Parametr **Zahrnout zaměstnance** se týká dodavatelů, kteří jsou propojeni s některým zaměstnancem. Můžete nastavit, zda tyto zaměstnance chcete zahrnout.

Proces vždy vyřadí takové dodavatele, u nichž je hodnota v poli **Blokování dodavatelů** nastavena na **Nikdy**.

Dodavatelé, kteří projdou ověřením, budou zablokováni, což nastaví hodnotu pole **Blokování dodavatelů** na **Všichni** a pole **Důvod** na to, co bylo zvoleno. Pro daného dodavatele se vytvoří záznam v historii blokování.

## <a name="vendor-invoice-account"></a>Účet dodavatele pro fakturaci
Pokud máte více než jednoho dodavatele se stejnou fakturační adresou, nebo pokud je dodavatel fakturován třetí stranou, můžete v záznamech dodavatele určit fakturační účet. Účtem faktury je účet, na který se připíše částka faktury po vytvoření faktury dodavatele z nákupní objednávky. Jestliže v záznamech dodavatele účet faktury nezadáte, potom se jako účet faktury použije účet dodavatele.

## <a name="vendor-bank-accounts"></a>Bank. účty dodavatele
Pokud je třeba provést platby na bankovní účet dodavatele, můžete zadat informace o bance a bankovních účtech dodavatele na stránce **Bankovní účty dodavatele**. Můžete také zadat informace o ověření a platbách na bankovním účtu. Můžete například k bankovnímu účtu dodavatele přidat verifikační transakce. Tyto verifikační transakce se používají k ověření přesnosti dat účtu, například směrovacích čísel nebo čísel účtů. Je nutné zadat výchozí účet pro platby dodavateli. Jakmile však budete realizovat samotnou platbu, můžete tento účet změnit na jeden z jiných účtů dodavatele.

## <a name="ledger-accounts"></a>Účty hlavní knihy
Můžete zadat výchozí účty, které se automaticky zobrazí v denících faktur daného dodavatele. Tato funkce může být užitečná, pokud průběžně obvykle platíte za stejné typy položek nebo služeb od stejných dodavatelů. Při určování výchozího účtu můžete rychle a efektivně zadat položky hlavního deníku do deníku faktury. Výchozí účty, které zadáte, nejsou použity pro nákupní objednávky, ani pro faktury dodavatele, které jsou zadány na stránce **Faktura dodavatele**.  

Vyberte výchozí účty na stránce **Výchozí nastavení účtu**, kterou lze otevřít na kartě **Faktura** v záznamech dodavatele. Účty, které zde vyberete, se při zadávání záznamu v deníku zobrazí ve filtrovaném seznamu účtů pro účet dodavatele. Jeden z účtů lze nastavit jako výchozí účet.



