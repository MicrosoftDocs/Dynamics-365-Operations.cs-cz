---
title: Účtování nepřímých nákladů
description: Tento článek vysvětluje, jak zaúčtovat nepřímé náklady, vytvořit nákladové skupiny a přidat uzly do nákladového formuláře pro nepřímé náklady.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868424"
---
# <a name="indirect-cost-posting"></a>Účtování nepřímých nákladů

Nepřímé náklady jsou náklady, které přímo nesouvisí s žádnou jednotlivou činností ve výrobním procesu. Příklady zahrnují administrativní náklady, jako jsou platy zaměstnanců, náklady účetního oddělení a režijní náklady, jako jsou nájemné, náklady na služby a stroje.

## <a name="calculating-indirect-costs"></a>Výpočet nepřímých nákladů

Microsoft Dynamics 365 Finance nemá automatizovaný způsob výpočtu sazby za nepřímé náklady. Musíte určit své nepřímé náklady, vytvořit kódy nepřímých nákladů a udržovat sazbu pro každý nepřímý náklad v nákladovém formuláři.

Přesný proces, který se používá k výpočtu nepřímých nákladů, se může mírně lišit společnost od společnosti. Obecně se však proces skládá z následujících základních kroků:

1. Vytvořte seznam nepřímých nákladů, které budou uznány ve výrobě. Tento seznam může zahrnovat nájemné, administrativní náklady, účetní poplatky a právní poplatky. Neměl by zahrnovat náklady na suroviny nebo mzdové náklady, které jsou uznány ve výrobních trasách.
2. Sečtěte všechny nepřímé náklady. Podobné typy nepřímých nákladů můžete seskupit nebo je ponechat oddělené. Každý konfigurovaný nepřímý náklad může mít různé hlavní účty, které se používají pro účtování do hlavní knihy.
3. Porovnejte nepřímé náklady s faktorem, který je také označován jako absorpční základna. Faktorem může být cokoliv, co si vyberete. Několik běžných příkladů:

    - Výnosy
    - Celkové množství, které se vyrábí
    - Přípravný čas
    - Operační čas

    Můžete si vybrat období, pro které chcete vypočítat nepřímé náklady, například měsíční, čtvrtletní nebo roční. Součet vašich nepřímých nákladů a součet vašeho faktoru by měl být za stejnou dobu. Pro výpočet sazby nepřímých nákladů se používá následující vzorec:

    *Míra nepřímých nákladů* = *Celkové nepřímé náklady* &divide; *Celkový faktor*

4. Vytvořte skupiny nepřímých nákladů.
5. Nakonfigurujte nákladový formulář se svými sazbami.
6. Udržujte náklady na nepřímé náklady ve verzi výpočtu nákladů.

> [!NOTE]
> Můžete použít modul **Nákladové účetnictví** pro akumulaci nákladů a stanovení vaší režie z různých zdrojů, jako je výroba, projekty a hlavní kniha. Podrobnější informace naleznete v tématu [Nákladové účetnictví](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Různá regulační zařízení zveřejnila pokyny o typech nákladů, které lze zahrnout jako nepřímé náklady nebo režijní náklady do nákladů na vaše hotové výrobky. Než začnete konfigurovat nepřímé náklady, doporučujeme, abyste se u svého účetního informovali o místních předpisech a ujistili se, že dodržujete.

## <a name="create-cost-groups-for-indirect-costs"></a>Vytvořte nákladové skupiny pro nepřímé náklady.

Musíte vytvořit alespoň jednu nákladovou skupinu, kterou chcete použít pro nepřímé náklady. Počet nákladových skupin, které můžete použít, není omezen. Zvažte, jak počítáte své náklady a zda existují různé sazby pro různé typy nákladů. Vaše organizace například vyrábí potravinářské produkty. Některé suroviny a hotové výrobky jsou suché zboží a mají jeden nepřímý náklad na skladování. Ostatní suroviny a hotové výrobky jsou chlazené a mají vyšší nepřímé náklady. V tomto případě možná budete chtít vytvořit dvě nákladové skupiny: **Režijní náklady na suchý materiál** a **Režijní náklady na chlazený materiál**.

Pokud chcete vytvořit nákladovou skupinu pro nepřímé náklady, postupujte takto.

1. Přejděte k **Řízení výroby &gt; Nastavení &gt; Postupy &gt; Skupiny nákladů**.
2. Volbou **Nová** vytvořte skupinu.
3. Do pole **Nákladová skupina** zadejte jedinečný název nákladové skupiny, například **MATOVH**.
4. Do pole **Název** zadejte popis nákladové skupiny, například **Režijní náklady na materiál**.
5. V poli **Typ nákladové skupiny** vyberte **Nepřímé**.
6. Volitelné: V poli **Chování** vyberte **Pevné náklady** nebo **Variabilní náklady**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Nakonfigurujte nákladový formulář pro nepřímé náklady

Po vytvoření jedné nebo více skupin nákladů můžete konfigurovat svůj nákladový formulář s nepřímými náklady a definovat svou kalkulaci. Možná budete chtít seskupit nepřímé náklady v nákladovém formuláři. Chcete-li seskupit nepřímé náklady, můžete vytvořit volitelné záhlaví v nákladovém formuláři. Pro každou nákladovou skupinu v nákladovém formuláři musíte vytvořit alespoň jeden uzel. Pro každou nákladovou skupinu pro nepřímé náklady můžete přidat další výpočty nepřímých nákladů.

### <a name="indirect-cost-node-types"></a>Typy uzlů nepřímých nákladů

Tato část popisuje různé typy uzlů pro nepřímé náklady.

#### <a name="surcharge"></a>Příplatek

**Příplatek** je jedním z nejběžnějších typů nepřímých nákladů. Vypočítává procento nákladů z absorpční základny nákladů na výrobní zakázce. Základ absorpce definujete výběrem skupin nákladů, které jsou propojeny s vašimi materiálovými nebo časovými složkami v nákladovém formuláři.

Například 3procentní přirážka může být přidána k výrobním nákladům za všechny suroviny na výrobní zakázce.

#### <a name="rate"></a>Sazba

Nepřímé náklady typu **Sazba** se používají k přidání fixní částky nákladů k výrobní zakázce z absorpční základny nákladů na výrobní zakázce. Sazba může být založena na jednom ze tří podtypů:

- **Proces** – Sazba je založena na době trvání trasy.
- **Nastavení** – Sazba je založena na přípravném čase trasy.
- **Množství** – Sazba je založena na vyrobeném množství.

Základ absorpce definujete výběrem skupin nákladů, které jsou propojeny s vašimi materiálovými nebo časovými složkami v nákladovém formuláři.

Ke každé výrobní zakázce je například přidána pevná částka 2,00 USD (USD) na základě doby běhu na trase pro skupinu mzdových nákladů ve vašem nákladovém formuláři.

#### <a name="output-unit-based"></a>Na základě výstupní jednotky

Nepřímé náklady typu **Na základě výstupní jednotky** se vypočítají vynásobením částky, která je uvedena na pevné záložce **Sazba** nákladového formuláře podle vybraného podtypu. Jako násobitel nepřímých nákladů můžete vybrat množství, hmotnost nebo objem hotového výrobku.

Množství například použijete k výpočtu 1,50 USD odpisů stroje pro každé vyrobené množství. Jako další příklad použijete objem k výpočtu 2,00 USD nákladů na chlazení pro objem prostoru, který hotové zboží zabere ve vašich chladicích jednotkách.

#### <a name="input-unit-based"></a>Na základě vstupní jednotky

Nepřímé náklady typu **Na základě vstupní jednotky** typ se vypočítá vynásobením množství surovin, které je spotřebováno na výrobní zakázce, množstvím. Pro výpočet součtu můžete použít hmotnost nebo objem vstupů na výrobní zakázce. Výpočet můžete omezit na podmnožinu materiálů výběrem jedné nebo více skupin nákladů na pevné záložce **Absorpční základ** nákladového formuláře.

Například použijete objem vstupů pro konkrétní nákladovou skupinu, která je spojena s chlazenými produkty, k přidání 1,00 USD k výrobní zakázce.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Vytvořte celkový uzel pro nepřímé náklady v nákladovém formuláři

Chcete-li vytvořit celkový uzel pro nepřímé náklady v nákladovém formuláři, postupujte takto.

1. Přejěte na **Cost management &gt; Nastavení účetních zásad nepřímých níkladů &gt; Nákladový formulář**.
2. Ve stromu vyberte uzel, který představuje náklady na zboží, které bylo vyrobeno.
3. Volbou **Nový** vytvořte uzel.
4. V poli **Vyberte typ uzlů** vyberte **Celkem**.
5. Do pole **Kód** zadejte jedinečné ID pro uzel, např. **Výrobní režijní náklady**.
6. Zaškrtněte políčko **Záhlaví**.
7. Zaškrtněte políčko **Celkem**.
8. Vyberte **OK**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Vytvořte skupinový uzel pro nepřímé náklady v nákladovém formuláři

Chcete-li vytvořit skupinový uzel pro nepřímé náklady v nákladovém formuláři, postupujte takto.

1. Přejěte na **Cost management &gt; Nastavení účetních zásad nepřímých níkladů &gt; Nákladový formulář**.
2. Ve stromu vyberte uzel, pod kterým chcete vytvořit nepřímé náklady. Vyberte například celkový uzel pro **Výrobní režijní náklady**.
3. Volbou **Nový** vytvořte uzel.
4. V poli **Vyberte typ uzlu** vyberte **Skupina nákladů**.
5. Do pole **Kód** zadejte jedinečné ID pro uzel, např. **TRASNSP**.
6. Do pole **Popis** zadejte stručný popis, například **Režijní náklady na dopravu**.
7. Vyberte **OK**.
8. V poli **Nákladová skupina** vyberte nákladovou skupinu, např. **OVH1: Režijní náklady na dopravu**.

### <a name="create-a-surcharge-indirect-cost"></a>Vytvořte příplatek za nepřímé náklady

Chcete-li vytvořit příplatek na nepřímé náklady v nákladovém formuláři, postupujte takto.

1. Přejěte na **Cost management &gt; Nastavení účetních zásad nepřímých níkladů &gt; Nákladový formulář**.
2. Ve stromu vyberte skupinový uzel nepřímých nákladů, pod kterým chcete vytvořit nepřímé náklady. Vyberte například celkový uzel pro **TRANSO - režijní náklady na dopravu**.
3. Volbou **Nový** vytvořte uzel.
4. V poli **Vyberte typ uzlů** vyberte **Příplatek**.
5. Do pole **Kód** zadejte jedinečné ID pro uzel, např. **Příplatek za dopravu**.
6. Vyberte **OK**.
7. V poli **Podtyp** vyberte **Celkem**.
8. Na pevné záložce **Absorpční základ** vyberte **Nový** a vytvořte kód nákladů.
9. V poli **Kód** vyberte nákladovou skupinu, kterou chcete použít pro výpočet přirážky.
10. Volitelné: Opakujte kroky 8 až 9 pro každou další skupinu nákladů, kterou chcete použít pro výpočet.
11. Na pevní záložce **Příplatek** vytvořte sazbu výběrem tlačítka **Nová**.
12. V poli **Verze** vyberte verzi kalkulace nákladu, ke které chcete přidat příplatek.
13. Volitelné: Do pole **Web** zadejte web, na který chcete příplatek uplatnit.
14. Do pole **Procento** zadejte procento pro výpočet výrobních zakázek z nákladových skupin, které jsou definovány na pevní záložce **Absorpční základ**.
15. Na pevní záložce **Zaúčtování do účetní knihy** vyberte hlavní účet, který chcete použít pro **Odhadované absorbované nepřímé náklady**, **Odhadované náklady spotřebovaných nepřímých nákladů, NV**, **Nepřímé náklady absorbovány** a **Náklady na spotřebované nepřímé náklady, NV**.
16. Volitelné: Na pevní záložce **Finanční dimenze** zadejte jakékoli finanční dimenze, které se mají standardně zadat u transakcí, když jsou zaúčtovány do hlavní knihy.

Předchozí postup ukazuje, jak vytvořit nepřímé náklady typu **Příplatek**. Podobné kroky se používají k vytváření dalších typů nepřímých nákladů. Následující části popisují rozdíly pro jednotlivé typy.

#### <a name="rate"></a>Sazba

- V kroku 4 vyberte **Sazba** namísto **Příplatek**.
- V kroku 7 vyberte **Proces**, **Založit** nebo **Množství** namísto **Celkem**.
- V kroku 11 použijte pevnou záložku **Sazba** místo pevné záložky **Příplatek**.
- V kroku 14 zadejte částku do pole **Množství** místo procenta v poli **Procento**.

#### <a name="output-unit-based"></a>Na základě výstupní jednotky

- V kroku 4 vyberte **Na základě výstupní jednotky** namísto **Příplatek**.
- V kroku 7 vyberte **Množství**, **Hmotnost** nebo **Objem** namísto **Celkem**.
- Přeskočte kroky 8 až 10.
- V kroku 11 použijte pevnou záložku **Sazba** místo pevné záložky **Příplatek**.

#### <a name="input-unit-based"></a>Na základě vstupní jednotky

- V kroku 4 vyberte **Na základě vstupní jednotky** namísto **Příplatek**.
- V kroku 7 vyberte **Hmotnost** nebo **Objem** namísto **Celkem**.
- V kroku 11 použijte pevnou záložku **Sazba** místo pevné záložky **Příplatek**.
