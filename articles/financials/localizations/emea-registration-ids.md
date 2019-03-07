---
title: ID registrace
description: Toto téma poskytuje informace o nastavení a používání ID registrace.
author: ShylaThompson
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7b663b9a72afdd3c2e2dcf503152f02e0b7861fd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "350497"
---
# <a name="registration-ids"></a>ID registrace

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace o nastavení a používání ID registrace.

Mnoho zemí a regionů má rozdílné předpisy a požadavky na evidenci daňového registračních čísel nebo ID. Toto téma obsahuje přehled požadovaných nastavení a zpracování typy podporovaných typů registrace pro účastníky v různých evropských zemích/oblastech. Všechny země/oblasti mají své požadavky na podporu různých funkcí v jednotlivých zemích týkající se registračních čísel uvedených různými státními úřady. Mezi příklady registračních čísel patří číslo sociálního pojištění (ČSP), daňové identifikační číslo (DIČ) a Evropské DPH identifikační číslo (EU DIČ). Tato funkce poskytuje jednotný rámec pro všechny země, ve všech oblastech, přičemž v úvahu bere požadavky specifické pro některé evropské země. V následujících částech je popsán celkový tok informací, které se používají k nastavení a zpracování ID registrace.

## <a name="registration-type-creation"></a>Vytvoření typu registrace
Dříve, než budete moci zadat ID registrace, je třeba nastavit typy registrace pro různé typy registračních čísel, kterým jednotlivé smluvní strany podléhají. Přejděte na stránku **Správa organizace** &gt; **Globální adresář** &gt; **Typy registrace** &gt; **Typy registrace** a vytvořte a spravujte typy registrace dodavatelů, odběratelů, zaměstnanců a právnických osob v různých zemích.

|Pole                 |popis      |
|------------------------------|----------------------------|                                                                           
| Jméno                | Název typu registrace. |                                                                           
| popis         | Popis typu registrace. |
| Země nebo oblast      | Jedná se o jednoznačnou identifikaci země nebo oblasti.|
| Finanční úřad       | Typ daňového úřadu, ke kterému je přidružen typ registrace.|
| Omezení       | Typ omezení, které platí pro typ daňové registrace: žádné, osoba, organizace.|
| Formát              | Formát ověření pro typ daňové registrace.|
| Lze aktualizovat.      | Definuje, zda lze registrační číslo aktualizovat po zadání pro typ daňové registrace.|
| Jedinečný              | Definuje, zda je registrační číslo pro typ daňové registrace jedinečné. |
| Primární pro zemi | Pokud je strana spojena s jednou nebo více adresami v konkrétní zemi a ID registrace je platné pro všechny tyto adresy, je třeba určit jednu adresu jako primární pro zemi. Můžete zaregistrovat pouze jedno ID jako primární. Určuje, zda lze zadat registrační číslo pouze pro primární adresu země. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Přiřazení typu registrace ke kategorii registrace
Registrace kategorie je identifikátor země registrace schválený pro používání v konkrétní zemi nebo oblasti pro daně, cla a jiné účely. Tato kategorie definuje pravidla ověření pro konkrétní ID registrace (včetně kontrolních číslic atd.) a zařazení ID registrace v různých sestavách. Na stránce **Správa organizace** &gt; **globální adresář** &gt; **typy registrace** &gt; **kategorie registrace** přiřaďte typ registrace konkrétní země registrace podporované kategorii.

| Pole            | popis|
|-----------------------|----------------|
| Typ registrace     | Typ registrace v konkrétní zemi nebo oblasti.|
| Omezení         | Typ omezení, které platí pro typ daňové registrace: žádné, osoba, organizace.|
| Kategorie registrace | Jedinečný identifikátor registrace schválený pro použití v dané zemi. Úplný seznam podporovaných v kategoriích Microsoft Dynamics 365 for Finance and Operations je níže. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Zadejte ID registrace pro záznamy globálního adresáře

Globální adresář (GAB) v aplikaci Microsoft Finance and Operations obsahuje konsolidované informace o adresách zákazníků, dodavatelů, kontaktů, obchodních vztahů a právnických osob. Další informace viz [Přehled globálního adresáře](../../fin-and-ops/organization-administration/overview-global-address-book.md). Záznamy strany, které jsou uloženy v globálním adresáři , mohou obsahovat jeden nebo více záznamů. Tyto adresy se používají k různým účelům, například k fakturaci nebo dodávce. Můžete nastavit registrační ID pro informace o adrese zákazníků, dodavatelů, pracovníků a právnických osob. Najděte záznam strany (právnická osoba, dodavatel, zákazník, pracovník), pro kterou chcete zadat ID registru, a klepněte na tlačítko **ID registrace** ve formulářích týkajících se strany, právnické osoby, dodavatele, zákazníka nebo pracovníka, k otevření stránky **Spravovat adresy**. Na kartě **Daňová registrace** klepněte na tlačítko **přidat** a zadejte následující informace o ID registrace.


|Pole                |popis                                                |
|---------------------|-----------------------------------------------------------|
| Typ registrace   | Typ registrace ve vybrané zemi nebo oblasti.     |
| Registrační číslo | ID registrace strany.                                |
| popis         | Popis registračního čísla.               |
| Sekce             | Další informace o registračních číslech. |
| Vydávající úřad      | Finanční úřad, který vydal registrační číslo.        |
| Datum vydání         | Datum vydání registračního čísla.              |
| Účinné:           | Datum platnosti registračního čísla.           |
| Vypršení platnosti          | Datum vypršení platnosti pro registrační číslo.          |

> [!NOTE]
> Číslo osvobození od daně právnické osoby, dodavatele a zákazníka lze vybrat z registračních ID souvisejících s DIČ a zadat pro danou stranu.

## <a name="search-for-records-by-registration-id"></a>Hledání záznamů podle ID registrace
Vyhledejte záznamy strany, které jsou založeny na ID registrace, je k dispozici ve formulářích týkající se strany, právnické osoby, dodavatele, zákazníka a pracovníka. Klepněte na tlačítko **Hledání ID registrace** k otevření stránky **Vyhledávací kritéria ID registrace**. Zadejte kritéria vyhledávání a klepněte na **najít**. Systém zobrazí vybrané záznamy z globálního seznamu adres a přidružených typů záznamu strany.

## <a name="supported-registration-categories"></a>Podporované kategorie registrací
V následující tabulce jsou uvedeny typy registrací podporovaných v aplikaci Finance and Operations. Pokud jste obeznámeni s poli aplikace Microsoft Dynamics AX 2012 pro ID registrace, tato tabulka také mapuje tato pole na kategorie registrace aplikace Finance and Operations.

| Kategorie registrace aplikace Finance and Operations         |Země nebo oblast  | Termín / pole Dynamics AX 2012|
|---------------------------------------------------------------|---------------------|---------------------------------|
| ID DPH                                                        | Všechny země Evropské unie (EU)|  Číslo osvobození od daně (právní typ ID daně v aplikaci AX 2012 R3)|
| Podnikové ID (COID)                                          | Belgie Česká republika Estonsko Maďarsko Lotyšsko Litva Polsko Švýcarsko | Číslo podniku (EnterpriseNumber) Registrační číslo (RegNum\_W) Registrační číslo (RegNum\_W) Registrační číslo (RegNum\_W) Registrační číslo (RegNum\_W) Číslo podniku (EnterpriseCode) Registrační číslo (RegNum\_W) UID (UID legislativního typu v aplikaci AX 2012 R3) |
| ID pobočky                                                     | Belgie            | Číslo pobočky (BranchNumber)|
| Spisová značka (registrační číslo, vydávající orgán, oddíl) | Česká republika     | Číslo vkladu (CommercialRegisterInsetNumber) Uchováváno v obchodním rejstříku (CommercialRegister) Oddíl obchodního rejstříku (CommercialRegisterSection)|
| Celní ID odběratele                                           | Finsko | Číslo odběratele pro celní účely (CustomsCustomerNumber\_FI)|
| DIČ                                                           | Ruská federace| INN (INN legislativního typu v aplikaci AX 2012 R3)|
| Kód důvodu registrace                                                           | Ruská federace| RRC (RRC legislativního typu v aplikaci AX 2012 R3)|
| OKDP                                                          | Ruská federace| OKDP (OKDP legislativního typu v aplikaci AX 2012 R3)|
| OKPO                                                          | Ruská federace| OKPO (OKPO legislativního typu v aplikaci AX 2012 R3)|
| RKOSU                                                         | Ruská federace| RCOAD (typ legislativním RCOAD v AX 2012 R3)|
| OGRN                                                          | Ruská federace| OGRN (OGRN legislativního typu v aplikaci AX 2012 R3) |
| SNILS                                                         | Ruská federace| SNILS (SNILS legislativního typu v AX 2012 R3)|
| CIFTS                                                         | Ruská federace| CIFTS (CIFTS legislativního typu v AX 2012 R3)|
| Pas                                                      | Španělsko             | Pas|
| Oficiální identifikační doklad                              | Španělsko             | Oficiální identifikační doklad|
| Certifikát o pobytu                                         | Španělsko             | Certifikát o pobytu|
| Jiný identifikační dokument                                 | Španělsko             | Jiný identifikační dokument|
| Nesečteno                                                  | Španělsko             | Není k dispozici v aplikaci AX 2012 R3|


Další informace o zpracování ID registrace, včetně nezbytných předpokladů, naleznete v následujících záznamech úloh pro ID DPH v Lifecycle Services (LCS):

-   Nastavení DIČ
-   ID registrace DPH dodavatele
-    Vyhledání strany pomocí DIČ




