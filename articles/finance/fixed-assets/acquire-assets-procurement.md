---
title: Pořízení majetku pomocí zásobování
description: Toto téma popisuje, jak integraci modulů Dlouhodobý majetek a Závazky nastavit tak, aby probíhalo automatické vytváření majetku z nákupních objednávek nebo faktur, případně automatické zaúčtování transakcí pořízení a opravy pořizovací ceny dlouhodobého majetku.
author: moaamer
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c51abd3ce380f0cb1ad688ffab16b239460bc45
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674740"
---
# <a name="acquire-assets-through-procurement"></a>Pořízení majetku pomocí zásobování

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak integraci modulů Dlouhodobý majetek a Závazky nastavit tak, aby probíhalo automatické vytváření majetku z nákupních objednávek nebo faktur, případně automatické zaúčtování transakcí pořízení a opravy pořizovací ceny dlouhodobého majetku. Jeden řádek nákupu vytvoří jeden majetek, bez ohledu na množství v řádku nákupu. Pokud potřebujete vytvořit několik dlouhodobých majetků, je nutné vytvořit několik řádků nákupu.

 K integraci dlouhodobého majetku a závazků jsou k dispozici následující metody a pro veškerý dlouhodobý majetek je nutné použít stejnou metodu:
-   Před přidáním čísla dlouhodobého majetku na řádek nákupní objednávky nebo faktury dodavatele vytvořte ručně dlouhodobý majetek. Transakce pořízení je automaticky zaúčtována při zaúčtování faktury dodavatele majetku. Toto je výchozí metoda.
-   Před přidáním čísla dlouhodobého majetku na řádek nákupní objednávky nebo faktury dodavatele vytvořte ručně dlouhodobý majetek. Při zaúčtování faktury dodavatele majetku není zaúčtována transakce pořízení.
-   Při zaúčtování příjemky produktu nebo faktury dodavatele se zaškrtnutým políčkem Vytvořit nový dlouhodobý majetek dojde k automatickému vytvoření nového dlouhodobého majetku. Transakce pořízení je automaticky zaúčtována při zaúčtování faktury dodavatele majetku.
-   Při zaúčtování příjemky produktu nebo faktury dodavatele se zaškrtnutým políčkem Vytvořit nový dlouhodobý majetek dojde k automatickému vytvoření nového dlouhodobého majetku. Při zaúčtování faktury dodavatele majetku není zaúčtována transakce pořízení.

Jestliže dáváte přednost ručnímu vytváření položek majetku, vyberte první nebo druhou metodu a potom přidejte číslo majetku do nákupní objednávky nebo faktury dodavatele. Jestliže upřednostňujete pružnější přístup, vyberte třetí nebo čtvrtou metodu. Někdy můžete položku majetku vytvořit ručně, jindy může být vytvořena automaticky na základě informací v detailech řádkové položky. 

Ať už položky majetku vytváříte ručně nebo používáte pružnější přístup, musíte rozhodnout, zda může být transakce pořízení zaúčtována pouze v modulu majetku, nebo při zaúčtování faktury dodavatele. V některých organizacích preferují ruční pořizování a vytváření transakcí pořízení uživateli do deníku nebo pomocí návrhů v modulu majetku. 

V tomto tématu jsou podrobně popsány obě metody.

## <a name="methods-for-manually-creating-fixed-assets"></a> Metody ručního vytvoření dlouhodobého majetku
Když zaúčtujete fakturu dodavatele, která má v řádcích uvedeno číslo majetku, a je zaškrtnuté políčko Povolit pořízení majetku v části Nakupování na stránce Parametry dlouhodobého majetku, pořízení je zaúčtováno automaticky a stav majetku se změní na hodnotu Otevřeno. 

Nemůže-li být pořízení zaúčtováno, můžete transakci pořízení zadat ručně v modulu majetku nebo můžete použít návrh pořízení v deníku modulu Dlouhodobý majetek k vytvoření více transakcí pořízení najednou.

> [!NOTE]                                                                                                                              
> Pokud je modul Dlouhodobý majetek nastaven tak, aby zaúčtování transakcí pořízení bylo omezeno na určitou skupinu uživatelů a vy chcete účtovat transakce pořízení z faktur, musíte být členem této skupiny.

## <a name="methods-for-automatically-creating-fixed-assets"></a> Metody automatického vytvoření dlouhodobého majetku
Při zaúčtování příjemky produktu, která má vybranou možnost Vytvořit nový dlouhodobý majetek pro řádek, vytvoří se nový dlouhodobý majetek se stavem Dosud nepořízený. Při zaúčtování faktury dodavatele za nový majetek dojde k zaúčtování transakce pořízení nového majetku. Pokud nastavení modulu Dlouhodobý majetek umožňuje pořizování majetku v modulu Závazky a jste členem skupiny uživatelů, která může účtovat transakce pořízení, změní se stav majetku na hodnotu otevřeno. 

Jestliže při zaúčtování příjemky produktu nebylo v řádku zaškrtnuté políčko Nový dlouhodobý majetek?, ale zaškrtli jste ho při zaúčtování faktury dodavatele, dojde k vytvoření a pořízení nového majetku se stavem Otevřeno za předpokladu, že nastavení modulu Dlouhodobý majetek umožňuje vytváření a pořizování majetku. Byl-li majetek vytvořen při zaúčtování příjemky produktu, při zaúčtování faktury dodavatele další majetek nevznikne.

### <a name="capitalization-threshold"></a>Prahová hodnota kapitalizace

Když používáte metodu automatického vytvoření a pořízení majetku, můžete nastavit, aby systém ověřil, zda pořizovací cena majetku odpovídá určité prahové hodnotě pro odpisování. Pokud tomu tak je, bude při vytvoření majetku z modulu Závazky vybraná možnost Odpis. 

Prahová hodnota kapitalizace je částka v měně, která určuje, zda je majetek odpisován, jestliže dosáhne zadané částky. Když například koupíte majetek a pořizovací cena je menší než prahová hodnota kapitalizace, majetek nebude odepisován. Pokud se pořizovací cena rovná nebo je větší než prahová hodnota kapitalizace, majetek se bude odepisovat. 

Prahovou hodnotu kapitalizace lze nastavit na stránce Skupiny dlouhodobého majetku.

## <a name="scenario"></a>Scénář
Následující scénář popisuje úplný cyklus integrace modulů Dlouhodobý majetek a Závazky. Dále je zde uvedeno vzorové nastavení a popsáno použití návrhů pořízení. 

Ve scénáři je použito následující nastavení systému:

-   Vytváření majetku je automatické a dochází k němu při zaúčtování příjemky produktu nebo faktury dodavatele. Nastavení modulu Dlouhodobý majetek neumožňuje účtování transakcí pořízení z modulu Závazky.
-   Účty jsou zadané v poli Typ účtu pro příjem dlouhodobého majetku a typy účtu Výdej dlouhodobého majetku na stránce Skupiny položek.
-   Prahová hodnota kapitalizace pro skupinu Počítače činí 1 500.
-   Vaším úkolem je zadat nákupní objednávku na nový laptop pro zaměstnance, objednávku zaúčtovat, ověřit, že příslušný pracovník zaúčtoval příjemku produktu, dále zaúčtovat fakturu a ověřit, že účetní aktualizovala stav nového laptopu na hodnotu Otevřeno.

Začněte na stránce Nákupní objednávka, do které zadejte podrobné informace o laptopu, jehož cena je 1 600. V řádku nákupní objednávky zaškrtněte políčko Nový dlouhodobý majetek? na pevné záložce Dlouhodobý majetek, vyberte skupinu majetku PC a objednávku uložte. 

Když laptop přijde, příslušný pracovník zadá a zaúčtuje příjemku produktu a tím zaznamená příjem laptopu. Položka majetku je vytvořena a je ve stavu Dosud nepořízeno. Částka překračuje prahovou hodnotu kapitalizace. Proto je zvolena možnost Odpis v knihách u laptopu. Vznikly následující transakce:

| Popis                               | Účet             | Má dáti    | Dal   |
|-------------------------------------------|---------------------|----------|----------|
| Nákup, nákup podle příjemky produktu        | Nefakturované příjmy | 1 600,00 |          |
| Nákup, protiúčet nákupu příjemky produktu | Časově rozlišené nákupy   |          | 1 600,00 |

Jako další krok zaúčtujete fakturu dodavatele za majetek. Stav laptopu se nezměnil, protože nastavení v modulu Dlouhodobý majetek neumožňuje zaúčtování transakce pořízení majetku při zaúčtování faktury dodavatele. Byla vybrána možnost Vytvořit nový dlouhodobý majetek při zaúčtování faktury dodavatele. Proto byl použit účet Příjem dlouhodobého majetku. Účet Výdej dlouhodobého majetku se nepoužil, protože se neúčtovalo o pořízení, ale bude použit později, až účetní zaúčtuje transakci pořízení pomocí návrhů pořízení v modulu Dlouhodobý majetek. 

Vznikly následující transakce:

| Popis                               | Účet             | Má dáti    | Dal   |
|-------------------------------------------|---------------------|----------|----------|
| Nákup, protiúčet nákupu příjemky produktu | Časově rozlišené nákupy   | 1 600,00 |          |
| Zůstatek dodavatele                            | Závazky    |          | 1 600,00 |
| Nákup, příjem dlouhodobého majetku             | Výdaje za počítače    | 1 600,00 |          |
| Nákup, nákup podle příjemky produktu        | Nefakturované příjmy |          | 1 600,00 |

Nakonec účetní zkontroluje všechny dlouhodobé majetky se stavem Dosud nepořízeno. Z toho vyplývá, že je nová položka majetku zkontrolována. Účetní otevře stránku Návrh pořízení z řádků deníku Dlouhodobý majetek a vytvoří transakce pořízení pro všechen majetek, ke kterému existují faktury, ale zatím je ve stavu Dosud nepořízený. Po zaúčtování deníku se stav majetku změní na Otevřeno. Účet Výdej dlouhodobého majetku bude kreditován a pořízení dlouhodobého majetku debetováno. 

Tento scénář může mít následující varianty:

-   Pokud je dlouhodobý majetek nastavena na povolení zaúčtování transakcí pořízení majetku při zaúčtování faktur dodavatele, účetní nemusí používat návrhy pořízení v modulu Dlouhodobý majetek, protože je vytvořena transakce pořízení. Dále budou aktualizovány různé účtů při zaúčtování dodavatelské faktury. Místo výdaje za počítače je debetován účet Příjem dlouhodobého majetku a proběhnou další dvě transakce: proběhne debetování účtu pro pořízení majetku a kreditování účtu pro výdej dlouhodobého majetku.
-   Není-li při zaúčtování příjemky produktu zaškrtnuto políčko Vytvořit nový dlouhodobý majetek, nevytvoří se v této chvíli žádný majetek. Zaškrtnete-li políčko Vytvořit nový dlouhodobý majetek před zaúčtováním faktury dodavatele, vytvoří se položka majetku se stavem Dosud nepořízený nebo se stavem Otevřeno, pokud při zaúčtování faktur dodavatele účtujete také transakce pořízení.
-   Pokud náklady na majetek jsou 1 400 místo 1 600, nebylo dosaženo prahové hodnoty kapitalizace. Proto je vytvořen majetek a zrušeno označení políčka Odpis.
-   Jestliže používáte registr faktur, po zaúčtování registru použijte k načtení dokladu stránku Deník schválených faktur, připojte nákupní objednávku k faktuře dodavatele, zaškrtněte políčko Vytvořit nový dlouhodobý majetek a potom fakturu dodavatele zaúčtujte. Pokud patříte do skupiny uživatelů, kteří mohou vytvářet transakce pořízení, vytvoří se pořízení a položka majetku bude mít stav Otevřeno.
-   Pokud je přijata pouze část množství, nedojde u první faktury dodavatele k pořízení majetku kvůli omezením skupin uživatelů. Jediný způsob, jak zaúčtovat pořízení u druhé faktury dodavatele, která doplní zbývající objednané množství, je, že musí být zadána transakce pořízení pro první fakturu dodavatele a musíte být členem skupiny uživatelů, kteří mohou účtovat pořízení.


Další informace naleznete v tématu [Integrace dlouhodobého majetku](fixed-asset-integration.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
