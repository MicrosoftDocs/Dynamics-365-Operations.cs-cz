---
title: Automatizace procesů inkasa
description: Tento článek popisuje, jak vytvořit strategie procesu inkasa, které automaticky identifikují faktury zákazníka, které vyžadují e-mailové připomenutí, aktivitu inkasa nebo odeslání upomínky zákazníkovi.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9ec749db197b4d04ee2e99ac7a16f4f2120c6707
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946140"
---
# <a name="collections-process-automation"></a>Automatizace procesů inkasa

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak vytvořit strategie procesu inkasa, které automaticky identifikují faktury zákazníka, které vyžadují e-mailové připomenutí, aktivitu inkasa (například telefonický hovor) nebo odeslání upomínky zákazníkovi. 

Organizace často tráví značné množství času zkoumáním sestav splatných zůstatků, zákaznických účtů a otevřených faktur, aby určily, které zákazníky je třeba kontaktovat ohledně otevřené faktury nebo zůstatku na účtu. Tento výzkum ubírá čas, který by inkasní agent mohl strávit komunikací se zákazníky za účelem shromažďování zůstatků po splatnosti nebo řešení sporů o faktury. Automatizace procesu inkasa vám umožňuje vytvořit strategický přístup k procesu inkasa. To vám pomůže konzistentně používat inkasní aktivity poskytnutím přizpůsobených e-mailových připomenutí nebo naprogramovaného procesu odesílání upomínek. 

## <a name="collections-process-setup"></a>Nastavení procesu inkasa
Můžete použít stránku **Nastavení procesu inkasa** (**Kredit a inkasa > Nastavení > Nastavení procesu inkasa**) k vytvoření automatizovaného procesu inkasa, který bude plánovat aktivity, odesílat e-mailové zprávy a vytvářet a zaúčtovávat upomínky zákazníka. Kroky procesu jsou založeny na přední nebo nejstarší otevřené faktuře. Každý krok používá tuto fakturu k určení, jaká komunikace nebo aktivita by měla probíhat s konkrétním zákazníkem.  

Týmy výběhu obvykle zasílají včasné oznámení týkající se každé nevyřízené faktury, aby byl zákazník informován, když má být faktura splatná. Výběr **Předupomínání** lze nastavit tak, aby umožňoval provedení jednoho kroku v každé hierarchii procesů pro každou fakturu, jakmile načasování faktury dosáhne tohoto kroku.

### <a name="process-hierarchy"></a>Hierarchie procesu
Každý fond zákazníků lze přiřadit pouze jedné hierarchii procesů. Pořadí hierarchie v tomto kroku určuje, který proces bude mít přednost, pokud je zákazník součástí více než jedné skupiny, která má přiřazenu hierarchii procesů. ID fondu určuje, kterým zákazníkům bude proces přiřazen. Každou nastavenou hierarchii plánování lze přiřadit pouze k jedné automatizaci procesu.

Tiché dny zajišťují, že zákazník není automatizovaným procesem kontaktován příliš často. Například pokud jsou tiché dny nastaveny na dva, nebude zákazník kontaktován automatizovaným procesem po dobu nejméně dvou dnů, a to ani v případě, že byla původní přední faktura vyrovnána v plném rozsahu. 

Chcete-li vyloučit zákazníky z automatizace procesu, pokud je zůstatek splatnosti zákazníka nebo částka faktury nižší než definovaná hodnota, vyberte **Splatný zůstatek zákazníka je nižší než** nebo **Částka faktury je nižší než** v poli **Vyloučit z procesu** a zadejte hodnotu částky.

Označením možnosti **Použít předpověď** vytvoříte aktivity inkasa pomocí předpovědi plateb zákazníků. Vytvořené aktivity budou používat šablonu Aktivita z **Předpovědí plateb** na stránce **Parametry pohledávek**, karta **Automatizace procesů inkasa**. 

### <a name="process-details"></a>Podrobnosti o procesu
Klikněte na **Nový** a přidejte do hierarchie nový detail procesu. **Popis** se používá k identifikaci účelu nebo názvu kroku v hierarchii. Vyberte **Typ akce** a definujte, zda krok vytvoří aktivitu, pošle e-mail nebo vytvoří upomínku. 

- **Obchodní dokument** definuje šablonu použitou k vytvoření typu akce. Tento dokument může být šablonou aktivity, šablonou e-mailu nebo upomínkou odeslanou každému zákazníkovi. Automatizace procesů inkasa vytváří pouze upomínky pro zákazníky bez ohledu na to, jak jsou nastaveny další parametry inkasa.
- **Když** definuje krok procesu, který proběhne před počátečním (nejstarším) datu splatnosti faktury nebo po něm a používá se společně s číslem zobrazeným ve sloupci **Dny ve vztahu k datu splatnosti faktury**. 
- Označte možnost **Předběžná upomínka** a vytvořte tak akci pro každou fakturu v jednom kroku hierarchie procesů. Akce předběžné upomínky jsou obvykle včasná oznámení týkající se nevyřízených faktur, aby byl zákazník informován, když se blíží datum splatnosti faktury. Předběžnou upomínku lze označit pouze pro jednu aktivitu na hierarchii. Když vyberete typ e-mailové akce, podle příjemce se určí, zda bude e-mailová zpráva odeslána zákazníkovi, prodejní skupině nebo inkasnímu agentu. 
- Hodnota v poli **Kontakt obchodního účelu** pak určí, který kontakt z účtu daného zákazníka obdrží komunikaci.

### <a name="business-document-details"></a>Podrobnosti obchodního dokumentu
Podrobnosti obchodního dokumentu se budou lišit podle typu akce, který je vybrán v podrobnostech procesu. Když je typ akce aktivita, zobrazí se podrobnosti šablony aktivity. Mezi tyto podrobnosti patří název šablony aktivity, typ aktivity, která bude vytvořena, účel aktivity, počet dní naplánovaných na dokončení aktivity a podrobnosti aktivity. Tato aktivita poté bude odkazovat na přední fakturu, která informuje příjemce o akci, která je k dokončení aktivity nutná.

Pokud je typ akce e-mail v podrobnostech procesu, bude tato část obsahovat dvě záložky s náhledem. První se používá k definování ID šablony, popisu e-mailu, výchozího jazyka, uživatelského jména, které bude přiřazeno automaticky odesílaným e-mailovým zprávám, a e-mailových adres přidružených odesílatelů. Na druhé lze vytvořit tělo e-mailu po uložení hodnot v polích **Jazyk** a **Předmět** výběrem volby **Upravit**. Otevře se okno, které umožňuje nahrát obsah HTML. 

> [!Note]
> E -mailovou zprávu aplikace Outlook, která obsahuje hlavní text komunikace, můžete uložit ve formátu HTML. Poté můžete nahrát obsah zprávy k implementaci šablony. <br> <br> Pokud je vybrán typ akce upomínky, ve stránce nastavení nebude sekce podrobností obchodního dokumentu.

Tlačítko **Historie procesu inkasa** použijte k zobrazení nedávné historie pro vybranou hierarchii procesů. 

Kliknutím na akci **Přiřazení procesu inkasa** zobrazíte zákazníky přiřazené k procesu inkasa. **Náhled přiřazení zákazníka** použijte k zobrazení hierarchie, které je přiřazen konkrétní zákazník. **Náhled procesu přiřazení** použijte k zobrazení náhledu zákazníků, kteří budou přiřazeni k hierarchii při jejím spuštění. Kliknutím na **Ruční přiřazení** zobrazíte zákazníky, kteří byli ručně přiřazeni k procesu, nebo vyberete zákazníky, kteří mají být přiřazeni k procesu.

Kliknutím na **Simulace procesů** zobrazíte náhled akcí, které budou vytvořeny, pokud je v tuto chvíli spuštěna automatizace vybraného procesu. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
