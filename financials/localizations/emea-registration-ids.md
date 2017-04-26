---
title: ID registrace
description: "Toto téma obsahuje informace o nastavení a používání ID registrace."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>ID registrace

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o nastavení a používání ID registrace.

Mnoho zemí a regionů mají rozdílné předpisy a požadavky na registrační číslo nebo ID záznamu. Toto téma obsahuje přehled požadovaných nastavení a zpracování typy podporovaných registrace pro účastníky v různých evropských zemích. Všechny země mají své požadavky pro podporu různých funkcí jednotlivých zemí týkající se registračních čísel uvedených různé státní úřady. Registrační čísla příklady, číslo sociálního pojištění (ČSP), daňové identifikační číslo (DIČ) a Evropské DPH identifikační (ID DPH EU). Tato funkce poskytuje jednotný rámec pro všechny země, ve všech oblastech, přičemž v úvahu požadavky specifické pro zemi některých evropských zemí. Následující oddíly popisují Celkový tok informací, která se používá pro nastavení a zpracování registrací ID.

## <a name="registration-type-creation"></a>Vytváření typu registrace
Před zadáním ID registrace, musíte nastavit typy registrace pro různé typy registračních čísel, které každá smluvní strana podléhá. Přejít na **Správa organizace**&gt;**globální adresář**&gt;**typy registrace**&gt;**typy registrace** stránku vytvořit a spravovat typy registrace dodavatelů, odběratelů, zaměstnanců a právnických osob v různých zemích.

|Pole                 |popis      |
|------------------------------|----------------------------|                                                                           
| Jméno                | Název typu registrace. |                                                                           
| popis         | Popis typu registrace. |
| Země nebo oblast      | Jedinečný identifikátor země/oblasti.|
| Finanční úřad       | Finanční úřad, který je přidružen k typu registrace.|
| Omezení       | Typ omezení, které platí pro tento typ daňové registrace: žádná osoba, organizace.|
| Formát              | Formát ověřování typu registrace.|
| Lze aktualizovat.      | Určuje, zda lze po zadání aktualizovat registrační číslo pro typ registrace.|
| Jedinečný              | Určuje, zda je jedinečné registrační číslo pro typ registrace. |
| Primární pro zemi | Pokud strana je spojen s jednou nebo více adres zejména země a ID registrace je platná pro tyto adresy, je třeba určit jednu adresu jako primární pro zemi. Můžete zaregistrovat pouze jedno ID jako primární. Určuje, zda číslo zápisu lze zadat pouze pro primární adresu země. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Přiřadit kategorie registrace typ registrace
Registrace kategorie je identifikátor země registrace schválena pro používání zejména země pro daňové, celní a jiné účely. Tato kategorie definuje pravidla ověření zvláštní registrační číslo (včetně kontrolní číslice atd.) a zařazení ID registrace v různých sestavách. Na stránce **Správa organizace**&gt;**globální adresář**&gt;**typy registrace**&gt;**kategorie registrace** přiřadit typ registrace konkrétní země registrace podporované kategorie.

| Pole            | popis|
|-----------------------|----------------|
| Typ registrace     | Registrace zadejte zejména země.|
| Omezení         | Druh omezení se vztahuje na typ daňové registrace: žádná osoba, organizace.|
| Kategorie registrace | Registrace jedinečný identifikátor schválených pro použití v zemi. Úplný seznam podporovaných v AX7.1 kategorie je níže. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Zadejte ID registrace pro záznamy knihy globální adresy
Globální adresář (GAB) 365 Microsoft Dynamics pro operace obsahuje adresu konsolidované informace pro zákazníky, dodavateli, kontakty, obchodní vztahy a právnické osoby. Další informace naleznete v [Přehled knihy globální adresy](/dynamics365/operations/organization-administration/overview-global-address-book). Záznamy strany, které jsou uloženy v globálním seznamu adres může obsahovat jeden nebo více záznamů adresu. Tyto adresy se používají k různým účelům, například k fakturaci nebo dodávce. Můžete nastavit registrační ID adresy informace pro zákazníky, dodavatele, pracovníky a právnické osoby. Strana (právnická osoba, dodavatele, zákazníka, pracovník) záznamu, pro který chcete zadat ID číslo registru a klepněte na tlačítko Najít **ID registrace** na formulářích týkající se strany, právnická osoba, dodavatele, zákazníka, pracovník otevřete **spravovat adresy** stránky. Na **daňové registrace** karta, klepněte na tlačítko **přidat**a zadejte následující informace o ID registrace.

|Pole                |popis                                                |
|---------------------|-----------------------------------------------------------|
| Typ registrace   | Typ registrace vybrané země nebo oblasti.     |
| Registrační číslo | ID registrace výrobce                                |
| popis         | Popis registrační číslo.               |
| Sekce             | Další informace o registrační číslo. |
| Vydávající úřad      | Orgánu, který vydal identifikační číslo.        |
| Datum vydání         | Datum vydání registračního čísla.              |
| Účinné:           | Datum platnosti registrační číslo.           |
| Vypršení platnosti          | Datum vypršení platnosti pro registrační číslo.          |

> [!NOTE]
> Daně, který číslo DIČ právnické osoby, dodavatele, zákazníka mohou být vybrány z registrace ID související s DPH ID a zadali pro stranu.

## <a name="search-for-records-by-registration-id"></a>Hledání záznamů podle ID registrace
Vyhledat záznamy strany, které jsou založeny na jediném ID registrace je k dispozici ve formulářích týkající se strany, právnická osoba, dodavatele, zákazníka a pracovníka. Klepněte na tlačítko **hledání ID registrace** otevřete **ID registrace vyhledávací kritéria** stránky. Zadejte kritéria vyhledávání a klepněte na **najít**. Systém zobrazí vybrané záznamy z globálním seznamu adres a přidružené typy záznamu strany.

## <a name="supported-registration-categories"></a>Kategorie podporovaných registrace
V následující tabulce jsou uvedeny typy podporovaných registrace v 365 Dynamics pro operace. Pokud jste obeznámeni s poli aplikace Microsoft Dynamics AX 2012 pro ID registrace, tato tabulka také mapuje 365 Dynamics pro operace zápisu kategorie těchto polí.

| Dynamics 365 pro kategorii operací zápisu         |Země nebo oblast  | Dynamics AX 2012 termín/pole|
|---------------------------------------------------------------|---------------------|---------------------------------|
| ID DPH                                                        | Všechny země Evropské unie (EU)|  DIČ (právní typ ID daně v AX2012 R3)|
| Podnikové ID (COID)                                          | Belgie, Česká republika Estonsko Maďarsko Lotyšska Litvy Polska Švýcarsko | Registrační číslo (EnterpriseNumber)-organizace (RegNum\_W) registrační číslo (RegNum\_W) registrační číslo (RegNum\_W) registrační číslo (RegNum\_W) registrační kód (EnterpriseCode)-organizace (RegNum\_W) UID (právní typ UID v AX2012 R3) |
| ID pobočky                                                     | Belgie            | Číslo pobočky (BranchNumber)|
| Spisová značka (registrační číslo, vydávající orgán, oddíl) | Česká republika     | Vsadit čísla Kept (CommercialRegisterInsetNumber) v obchodním registru oddíl (CommercialRegister) v obchodním rejstříku (CommercialRegisterSection)|
| Celní ID odběratele                                           | Finsko | Celní číslo odběratele (CustomsCustomerNumber\_FI)|
| DIČ                                                           | Ruská federace| INN (typ legislativním INN v AX2012 R3)|
| Kód důvodu registrace                                                           | Ruská federace| Kód důvodu registrace (právní typ kódu důvodu registrace v AX2012 R3)|
| OKDP                                                          | Ruská federace| OKDP (typ legislativním OKDP v AX2012 R3)|
| OKPO                                                          | Ruská federace| OKPO (typ legislativním OKPO v AX2012 R3)|
| RKOSU                                                         | Ruská federace| RCOAD (typ legislativním RCOAD v AX2012 R3)|
| OGRN                                                          | Ruská federace| OGRN (typ právních OGRN v AX2012 R3) |
| SNILS                                                         | Ruská federace| SNILS (typ právních SNILS v AX2012 R3)|
| CIFTS                                                         | Ruská federace| CIFTS (typ právních CIFTS v AX2012 R3)|

Další informace o ID registrace zpracování, včetně nezbytné součásti naleznete v tématu následující záznamy úkolu ID DPH v Lifecycle Services (LCS):

-   Nastavení DIČ
-   Registrace DIČ dodavatele
-    Vyhledání strany pomocí DIČ





