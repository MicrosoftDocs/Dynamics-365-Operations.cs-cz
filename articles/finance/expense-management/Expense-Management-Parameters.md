---
title: Parametry správy výdajů
description: Chování v modulu Správa výdajů řídí následující parametry.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c1bc754b92e647f0fdac6799564273fb6ea6fb20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176789"
---
# <a name="expense-management-parameters"></a>Parametry správy výdajů

[!include [banner](../includes/banner.md)]

-----------------------------

Obecné chování v modulu Správa výdajů řídí následující parametry.

### <a name="general"></a>Obecné

| **Pole**                                                | **Popis**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardní sazba za míli**                             | Zadejte sazbu refundace výdajů za ujeté kilometry. Sazba bude vynásobena vzdáleností zadanou ve výdajích při výpočtu částky uhrazené za cestovní výdaje.                       |
|**Osobní výdaje hradil**                             | Vyberte, kdo je odpovědný za zaplacení jakékoli částky transakce platební karty kategorizované jako osobní.                                                                                                     |
|**Zobrazit celou sestavu výdajů ve zpětném rozboru**               | Tuto možnost vyberte, chcete-li zobrazit všechny výdaje pro vyúčtování výdajů při zobrazení podrobností o původním dokumentu dokladů konkrétního poukazu generovaného při zaúčtování vyúčtování výdajů.              |
|**Předběžná autorizace cesty je povinná.**                 | Tuto možnost vyberte, chcete-li vyžadovat, aby byla cestovní žádanka odeslána a schválena předtím, než zaměstnanec může odeslat vyúčtování výdajů.                                                                    |
|**Povolit úpravy distribucí před zaúčtováním**            | Určete, zda lze před zaúčtováním upravit distribuce vyúčtování výdajů.                                                                                                                 |
|**Vyhodnotit zásady správy výdajů**                     | Vyberte, kdy byly posouzeny náklady, které jsou vyhodnoceny k určení, zda došlo k porušení zásad výdajů. Případná porušení výdajů lze zkontrolovat při zadání a uložení položky vyúčtování výdajů nebo při odeslání výdaje ke schválení. Pravidla zásad pro požadované příjmy budou zkontrolována při uložení řádku výdajů.                   |
|**Povolit řádky mezipodnikových výdajů**                         | Vyberte, zda chcete povolit zápis výdajů pro další právnické osoby v rámci vyúčtování výdajů.                                                                                                          |
|**Povolit úpravy směnného kurzu pro výdaje z platební karty** | Tuto možnost vyberte, chcete-li umožnit uživatelům úpravu směnného kurzu pro výdaje kreditní kartou.                                                                        |
|**Pole víceúrovňové hierarchie k zobrazení**                  | Vyberte, která pole schvalovatele se mají zobrazit při nastavení typu přiřazení workflowu na hierarchické a nastavení výběru hierarchie na používání hierarchie schvalování výdajů na více úrovních. Při použití víceúrovňové hierarchie schválení u workflowu se zobrazí vybraná pole a bude je možné ve vyúčtování výdajů upravovat. |
|**Zadejte číslo platební karty zaměstnance (aktualizace z července 2017)**     | Vyberte, zda je možné zadat číslo o velikosti 15 nebo 16 znaků a zda je možné ho uložit do pole **ID karty** na stránce **Platební karty** zaměstnance.                                                                          |

### <a name="financial"></a>Finanční

| **Pole**                                                            | **Popis**     |
|----------------------------------------------------------------------|------------------------------------|
|**Název deníku hlavní knihy**                                         | Vyberte název deníku hlavní knihy, do kterého jsou zaúčtována schválená vyúčtování výdajů.            |
|**Povolit vratku daně z výdajů**                                  | Výběrem této možnosti povolíte vratku daně výdajů u oprávněných výdajů. Tuto možnost nelze povolit, pokud jsou povolena pravidla pro daň z prodeje v USA a importní DPH.      |
|**Zaúčtovat ihned hotovostní zálohy**                                     | Vyberte tuto možnost, pokud chcete zaúčtovat schválenou hotovostní zálohu po dokončení procesu platby a převodu. Pokud tato možnost není vybraná, proces platby a převodu vygeneruje nezaúčtovaný hlavní deník. |
|**Opravit datum účtování během zaúčtování**                             | Tuto možnost vyberte, pokud chcete aktualizovat datum účtování při zaúčtování nákladů, pokud je aktuální období blokované nebo uzavřené. Datum účtování se nastaví na další otevřené období.   |
|**Povolit seskupování transakcí podle protiúčtu určeného v rámci způsobu platby**      | Vyberte tuto možnost, chcete-li sečíst výdajové transakce pro sestavu výdajů na základě protiúčtu zadaného ve způsobu platby pro výdaje.   
|**Včetně daně**                                                   | Tuto možnost vyberte pro zahrnutí DPH do částky výdajů ve výchozím nastavení.             |
|**Uvolnit břemena na uzavírání cestovních žádanek**            | Tuto možnost vyberte pro uvolnění financí s břemenem při uzavření schválené cestovní žádanky.                                                                                   |
|**Umožnit odesílání cestovních žádanek při překročení rozpočtu registru a rozpočtu projektu** | Zaškrtnutím tohoto políčka umožníte zaměstnancům odeslat cestovní žádanky ke schválení, které překročí buď povolený rozpočet, který je nastavený v registru rozpočtu nebo povolený rozpočet projektu.            |
|**Umožnit odesílání sestav výdajů při překročení rozpočtu registru a rozpočtu projektu**    | Zaškrtnutím tohoto políčka umožníte zaměstnancům odeslat vyúčtování výdajů ke schválení, které překročí buď povolený rozpočet, který je nastavený v registru rozpočtu nebo povolený rozpočet projektu.                |
|**Umožnit schválení vyúčtování výdajů pouze při překročení rozpočtu registru**                | Vyberte tuto možnost, chcete-li povolit schvalujícím schvalovat vyúčtování výdajů, které překračují povolený rozpočet, který je nastavený v registru rozpočtu.                                                                       |

### <a name="per-diem"></a>Denní diety

| **Pole**                             | **Popis**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimální hodiny pro denní diety**           | Zadejte výchozí minimální počet hodin, které zaměstnanec musí odpracovat v jednom dni, aby mu vznikl nárok na denní diety související s cestovními výdaji.  Tato hodnota slouží pouze jako výchozí hodnota pro pole Minimální hodiny pro úrovně sazeb denních diet.                                                                                      |
|**Procento za jídlo**                          | Zadejte výchozí procento denní diety za stravování, používané první a poslední den související cestovních výdajů, když je hodnota v poli **srážka na stravné ve výpočtu** nastavená na **Typ jídla na den** nebo **Počet jídel za den**. Pracovní den pro první a poslední den může být kratší než standardní pracovní den. Částka denní diety pro tyto dny se tedy může lišit od paušální částky. Je-li procento nastaveno na hodnotu 0, odpočty první a poslední den budou 0,00. |
|**Procentuální částka za hotel**                        | Zadejte výchozí procento diety v hotelích, které se použije pro první a poslední den související cestovních výdajů. Pracovní den pro první a poslední den může být kratší než standardní pracovní den. Částka denní diety pro tyto dny se tedy může lišit od paušální částky. Je-li procento nastaveno na hodnotu 0, odpočty první a poslední den budou 0,00.                                              |
|**Ostatní procentuální částka**                        | Zadejte výchozí procento diety pro různé výdaje, které se použije pro první a poslední den výdajů v hotelích. Pracovní den pro první a poslední den může být kratší než standardní pracovní den. Částka denní diety pro tyto dny se tedy může lišit od paušální částky. Je-li procento nastaveno na hodnotu 0, odpočty první a poslední den budou 0,00.                                                                                                     |
|**Snížení za snídani (v procentech)** | Zadejte částku snížených denních diet za snídani. Dochází-li například zaměstnanec na snídaně v rámci ubytování, můžete zde snížit částku diety o 10 procent.                               |
|**Snížení za oběd (v procentech)**    | Zadejte částku snížených denních diet za oběd. Dochází-li například zaměstnanec na obědy v rámci ubytování, můžete zde snížit částku diety o 15 procent.                                       |
|**Snížení za večeři (v procentech)**   | Zadejte částku snížených denních diet za večeři. Dochází-li například zaměstnanec na večeře v rámci ubytování, můžete zde snížit částku diety o 25 procent.                                     |
|**Vypočítat srážku za stravné pomocí**         | Vyberte způsob výpočtu snížení diet za jídlo výběrem snížení, pokud je založeno na typu jídlo na kalendářní den cesty nebo pokud je snížení založeno na počtu povolených denních jídel.|
|**Zaokrouhlení denních diet**                  | Vyberte typ zaokrouhlení používaný pro výdaje denních diet. Pokud vyberete normální zaokrouhlení, jakýkoli výdaj na dietu, který má částku 0,50, se zaokrouhlí na hodnotu 1,00 a jakýkoli výdaj za dietu, který má částku nižší než 0,50, je zaokrouhlen na 0,00.                                                                                              |
|**Základ pro výpočet denních diet**         | Vyberte, zda jsou výpočty denních diet založeny na období 24 hodin nebo na kalendářním dni.       |

### <a name="fax-cover-pages"></a>Faxovat titulní stránky

| **Pole**                      | **Popis**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instrukce**                   | Zadejte pokyny, které zaměstnanci musí dodržovat při vytváření titulní stránky faxu, která slouží k odeslání účtenek, které se vztahují k vyúčtování výdajů. Klepněte na tlačítko **Překlady**, pokud chcete zadat text pro konkrétní jazyk, který bude zobrazen na základě jazyka uživatele. |
|**ID uživatele (informace v čárovém kódu)** | Tuto možnost vyberte pro uložení jedinečného identifikátoru zaměstnance do čárového kódu, který se používá na titulní stránce faxu.                 |
|**Čárový kód**                      | Vyberte čárový kód, který se používá pro titulní stránku faxu. Čárové kódy 39 a 128 jsou podporované v modulu Správa výdajů.               |

### <a name="anti-corruption"></a>Protikorupční

|                 <strong>Pole</strong>                 |                                                                                                                                                                                            <strong>Popis</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Zobrazit protikorupční osvědčení</strong>  | Tuto možnost vyberte, chcete-li zobrazit odesílatel protikorupčního textu při vytváření nové sestavy výdajů. Následně lze povolit konkrétní kategorie výdajů, které budou vyžadovat protikorupční atestaci pro výběr na vyúčtování výdajů. Například kategorie daru související s výdaji na státního úředníka, mohou vyžadovat, aby zaměstnanec potvrdil, že vyúčtování výdajů splňuje zásady společnosti týkající se státních úředních osob. |
| <strong>Protikorupční zpráva pro odesílatele</strong> |                                                                                             Zadejte text, který se zobrazí zaměstnanci při vytváření nové sestavy výdajů. Klepněte na tlačítko <strong>Překlady</strong>, pokud chcete zadat text pro konkrétní jazyk, který bude zobrazen na základě jazyka uživatele.                                                                                             |
| <strong>Protikorupční zpráva pro schvalovatele</strong>  |                                                                                             Zadejte text, který se zobrazí schvalujícímu při vytváření nové sestavy výdajů. Klepněte na tlačítko <strong>Překlady</strong>, pokud chcete zadat text pro konkrétní jazyk, který bude zobrazen na základě jazyka uživatele.                                                                                             |

