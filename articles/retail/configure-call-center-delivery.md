---
title: Konfigurace způsobů dodání a poplatků call centra
description: Toto téma popisuje způsob nastavení režimů dodání a poplatků objednávky kontaktního střediska v Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2571b4ffd6c13dbf755ef2dfa93b757822890d96
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553592"
---
# <a name="configure-call-center-delivery-modes-and-charges"></a>Konfigurace způsobů dodání a poplatků call centra

[!INCLUDE [banner](includes/banner.md)]

Když je zadaná objednávka v aplikaci Microsoft Dynamics 365 for Retail a osoba, která ji zadala, je spojená s kanálem kontaktního centra, je použita logika a pravidla k ověření způsobu dodání a výpočtu poplatků za objednávku.

Když vytvoříte prodejní objednávku, můžete vybrat způsob dodání v záhlaví prodejní objednávky a řádku prodejní objednávky. Výchozí způsob dodání, který jste vybrali v záhlaví, se používá pro všechny řádky prodejní objednávky. Lze však přepsat výchozí způsob dodání v jednotlivých řádcích prodejních podle potřeby. Rovněž můžete definovat způsob dodání v záznamu odběratele. Potom, když jsou vytvářeny objednávky pro zákazníka, je tento režim dodání použit ve výchozím nastavení v záhlaví prodejní objednávky.

Retail obsahuje funkce, které umožňují uživatelům omezit způsoby dodání, které jsou platné pro konkrétní místa expedice, způsoby dodání, které lze použít v některém kanálu a způsoby dodání, které lze použít pro produkt. Náklady lze definovat také tak, aby byly přidány další poplatky do objednávky zákazníka na základě režimů doručení, které jsou vybrány pro prodejní objednávku a celkovou hodnotu objednávky.

## <a name="define-delivery-modes"></a>Definování režimů dodání

Dříve než určíte dodání, které režimy dodání lze použít pro objednávky call centra a definujete přidružené náklady a pravidla, je nutné definovat způsoby dodání. Přejděte na **Prodej a marketing\> Nastavení \> Distribuce \> Způsoby dodání**. Nový způsob dodání vytvoříte kliknutím na položku **Nový**. Nebo vyberte existující režim dodání v seznamu a pak vyberte **upravit** k provedení změn.

V poli **způsob dodání**, zadejte veškeré kombinace s alfanumerickými znaky založené na vašem obchodní požadavku. Poté můžete vybrat pole **popis** pro zadání dalších kontextu. Pole **Skupina nákladů** a **urychlené zpracování** jsou volitelná a budou vysvětlena podrobněji dále v tomto tématu.

Na pevné záložce **maloobchodní kanály** přidejte maloobchodní kanál, který by měl mít povoleno použít režim dodání, když jsou transakce vytvořeny v daném kanálu.

Na pevné záložce **produkty** můžete určit, pro které produkty nebo kategorie produktů lze režim dodání použít a pro které ne. Například pokud produkt nelze expedovat letecky z důvodu nebezpečného materiálu (hazmat), ujistěte se že produkt nebo skupinu produktů je vyňat z všech způsobů dodání zahrnujících leteckou přepravu.

Na pevné záložce **Adresy** můžete určit, pro které země, regiony nebo státy lze režim dodání použít a pro které ne. Například objednávky, které jsou odesílány na Havajské ostrovy nebo Aljašku, nemají nárok na doručení po zemi. Proto by měly být tyto státy vyloučeny z jakéhokoli režimu dodání, který je spojen se službou pozemního dodání, ale jsou zahrnuty do jakéhokoli režimu dodání, který je spojený se službou leteckého dodání.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Ověření způsobů dodání pro objednávku kontaktního střediska

Poté, co jsou definovány způsoby dodání, je nutné spustit dávkovou úlohu **zpracování způsobů dodání**. Tato úloha ke zpřístupní dostupné způsoby dodání, aby bylo možné je použit v procesech prodejní objednávky pro maloobchodní kanály. Aby bylo možné spustit úlohu **zpracování způsobů dodání**, přejděte na **maloobchod \> maloobchodní IT \> zpracování způsobů dodání**. Tento úkol by měl být spuštěn pokaždé, když jsou přidány nové způsoby dodání do maloobchodní sítě nebo jsou provedeny změny existujících vztahů režimu/kanálu dodání.

Po spuštění dávkové úlohy **zpracování způsobů dodání** můžete přejít na **maloobchod \> kanály \> kontaktní střediska \> všechna kontaktní střediska**. Na stránce **všechna kontaktní střediscka** v podokně akcí na kartě **nastavení** vyberte **způsoby dodání**. Stránka **Způsoby dodání** uvádí všechny platné způsoby dodání pro vybraný kanál call centra. Chcete-li upravit existující způsoby dodání nebo přidat nové způsoby dodání, vyberte **Správa způsobů dodání**. Všimněte si, že úlohu **zpracování způsobů dodání** je nutné provést při každé změně.

## <a name="define-charges-for-delivery-services"></a>Definování nákladů na služby dodání

Při vytváření prodejních objednávek pro odběratele může společnost chtít přidat náklady, které se vypočítávají automaticky podle způsobů dodání, které jsou vybrány pro objednávku. Tyto náklady lze konfigurovat tak, aby byly stejné pro všechny zákazníky a způsoby dodání. Případně se náklady mohou lišit v závislosti na odběrateli a způsobech dodání, které jsou vybrány pro prodejní objednávku.

Pokud chcete definovat náklady, přejděte na **maloobchod \> nastavení kanálu \> náklady \> automatické náklady**. Vyberte **nový** pro přidání nových nákladů. Nebo vyberte existující položku a poté vyberte **upravit**.

Náklady lze definovat tak, aby byly vypočteny na úrovni záhlaví objednávky nebo řádků objednávky. V poli **úroveň** vyberte požadovanou úroveň.

Náklady lze definovat pro konkrétního zákazníka, skupinu zákazníků nebo všechny zákazníky. V poli **kód účtu** vyberte **tabulka** k definování nákladů, které platí pouze pro specifické odběratele. Vyberte **skupina** k definování nákladů pro určité skupiny. Vyberte **všechny** k použití nákladů pro všechny odběratele, kteří zadají prodejní objednávku, která používá související způsob dodání. Pokud jste vybrali **tabulka** nebo **skupina** v poli **kód účtu**, vyberte odběratele nebo skupinu odběratelů v poli **vztah účtu**.

Náklady lze konfigurovat tak, aby se použily pro konkrétní způsob dodání, skupinu režimu dodání nebo všechny způsoby dodání. Vyberete-li **tabulka** v poli **kód způsobu dodání**, je nutné vybrat konkrétní způsob dodání v poli **vztah způsobu dodání**. Vyberete-li **skupina**, je nutné vybrat skupinu v režimu dodání v poli **vztah způsobu dodání**. Skupiny způsobů dodání jsou definovány ve skupině **maloobchod \> nastavení kanálu \> náklady \> skupina nákladů na dodání**. Lze pak je navzájem propojit s jedním nebo více způsoby dodání na stránce **způsoby dodání**. Pokud při definování nákladů vyberte skupinu, používá tyto náklady jakýkoli způsob dodání, který je připojen k vybrané skupině dodání. A nakonec pokud v poli **Kód způsobu dodání** vyberete možnost **Vše**, budou náklady používat všechny režimy dodání. Proto nevybírejte hodnotu v poli **vztah způsobu dodání**.

V oddílu **řádky** lze definovat jeden nebo více nákladů podle měny, jak potřebujete. Náklady musí být spojeny s kódem nákladů, který definuje pravidla zaúčtování pro náklady. Pole **Kategorie** se používá k definování, jak byly vypočítány náklady. Pokud by například mělo být zákazníkovi účtováno 9,95 USD, aby mu byla expedována objednávka podle konkrétního způsobu dodání, použijte kategorii **Pevné**. Pokud se firma rozhodne zpoplatnit odběratele procentem celkové částky objednávky k pokrytí nákladů na dodání, použijte kategorii **procento**. Skutečné náklady pro odběratele jsou definovány v poli **náklady**.

Maloobchodní společnosti často konfigurují vrstvené poplatky. Částka, kterou odběratelé platí za dodání, je v tomto případě založena na hodnotě objednávky. Chcete-li konfigurovat vrstvené poplatky, zadejte hodnoty do pole **od částky** a **do částky** a také definujte náklady na vlastní poplatky v poli **náklady**. Například u objednávek, které mají hodnotu, která je nižší než $50, účtuje prodejce $5,95 pro expedici po zemi. Pro objednávky, které mají hodnotu, která je rovno nebo větší než $50, ale méně než $100, prodejce účtuje $7.95. A nakonec pro objednávky, které mají hodnotu, která je rovna nebo větší než $100, prodejce poskytuje dodání zdarma. Následující obrázek znázorňuje konfiguraci těchto nákladů.

![Příklad pevných vrstvených poplatků](media/fixedtieredcharges.png)

Můžete vybrat kombinaci kategorie nákladů, v závislosti na požadavcích vaší společnosti. Například u všech objednávek, které mají hodnotu, která je nižší než $100, se účtuje pevný poplatek ve výši $9,95 za dodání. Poté pro objednávky, které mají hodnotu, která se rovná nebo je větší než $100, jsou náklady na dodání vypočítávány ve výši hodnoty objednávky. Následující obrázek znázorňuje konfiguraci těchto nákladů.

![Příklad kombinovaných vrstvených poplatků](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Použití způsobů dodání během zadání objednávky v kontaktním středisku

Při vytvoření nové prodejní objednávky musí být zadána hodnota v poli **způsob dodání** na pevné záložce **dodání** záhlaví prodejní objednávky. Tato pole může být vyplněno automaticky podle výchozích hodnot ze záznamu odběratele.

Způsob dodání, který je definován v záhlaví objednávky, je automaticky zkopírován do řádků prodejní objednávky při jejich vytváření. Nastavení způsobu dodání pro určitou položku řádku lze však změnit na kartě **dodání** v části **podrobnosti řádku** na stránce zadávání prodejní objednávky.

Pokud vybraný způsob dodání pro vybraný produkt nebo adresu dodání, které jsou definovány pro objednávku nebo řádek objednávky, není platný, zobrazí se chybová zpráva. Potom je nutné vybrat způsob dodání, který byl definován pro tento produkt nebo konfiguraci adresy.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Výpočet nákladů na dodání během zadání objednávky

Pokud je zapnuto nastavení **povolit dokončení objednávky** pro kontaktní středisko, dopravné bude automaticky vypočítáno pro prodejní objednávky, když uživatel vybere **Dokončit**. Tato zpráva se zobrazí v horní části stránky **souhrn prodejní objednávky**: "Vypočítané vrstvené náklady." Vypočtené náklady jsou přidány k hodnotě pole **prodeje celkem**. Na pevné záložce **částka** pole **náklady** zobrazuje celkovou částku všech nákladů, které byly vypočteny pro objednávku a řádky. Chcete-li zobrazit podrobnější rozdělení nákladů, vyberte **objednávka** na stránce **souhrn prodejní objednávky** a poté vyberte možnost **náklady** k zobrazení, přidání nebo úpravě nákladů. Všimněte si, že výpočet nákladů na dodání v záhlaví objednávky je založen na způsobu dodání, která je připojena k záhlaví. Náklady na dodání na úrovni řádku se vypočítávají podle způsobu dodání, nastaveného pro prodejní řádek. Jestliže se používá několik způsobů dodání na různých řádcích, více nákladů může být použito a sečteno. Celková částka je pak uvedenya v poli **náklady** na stránce **souhrn prodejní objednávky**.

Pokud je nastavení **povolit dokončení objednávky** vypnuté, uživatelé musí ručně spustit výpočet nákladů. Na stránce **Prodejní objednávka** v podokně akcí na kartě **Prodej** ve skupině **Vypočítat** vyberte **Vrstvené náklady**. Zobrazí se zpráva "vypočítány vrstvené náklady". Pak můžete vybrat možnost **náklady** na kartě **Prodej**, abyste mohli zobrazit, upravit nebo odstranit vypočtené náklady.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Použití urychlených způsobů dodání u objednávek kontaktního střediska

Volitelně můžete propojit kód urychleného zpracování u libovolného způsobu dodání, který konfigurujete. Tento kód se používá jako nástroj ke stanovení priority řazení a vykazování. Nezpůsobí aktuálně použití dalších poplatků pro objednávku. Chcete-li nastavit kódy urychleného zpracování, přejděte na **prodej a marketing \> nastavení \> distribuce \> kódy urychleného zpracování**.

Například pro objednávky, které budou expedovány letecky další den, výdej je zapotřebí provést ze skladu do 13: 00 každý den. V takovém případě lze vytvořit kód urychleného zpracování a kód lze spojit s libovolným způsobem dodání další den, konfigurovaným v systému. Když se ve skladu vytvoří vlna výdeje, příslušný kód urychleného zpracování v poli **urychlené zpracování** lze použít jako filtr, aby byl běh výdeje jen pro objednávky, které mají způsob dodání spojený s tímto kódem.

Dále platí, že při zadání objednávky kontaktního střediska, lze kód urychleného zpracování použít ručně v záhlaví prodejní objednávky nebo na samostatném řádku prodejní objednávky. Kód lze použít k třídění nebo pro účely vykazování. V některých případech musí být objednávka zpracována pečlivě z důvodu problému se službou odběratele. V takovém případě lze v záhlaví nebo na řádkách objednávky použít konkrétní kód urychleného zpracování na pomoc se stanovením prioritního pořadí při procesu plnění.
