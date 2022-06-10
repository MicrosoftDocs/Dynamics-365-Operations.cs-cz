---
title: Zaúčtování výrobní zakázky
description: Toto téma obsahuje informace o různých typech zaúčtování výrobní zakázky.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: cd1b6c49e59f9480fd831ad5ff143033ca09792c
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/24/2022
ms.locfileid: "8802982"
---
# <a name="production-postings"></a>Zaúčtování výroby

Toto téma obsahuje informace o různých typech zaúčtování v procesu výrobní zakázky.


## <a name="material-consumption"></a>Spotřeba materiálu

Materiály jsou při výrobě registrovány jako spotřebované, když je zaúčtován deník výrobních výdejek. Vytvoří se tak transakce, které se odečtou od zásob na skladě. V **Parametrech výroby** můžete určit, zda hodnota surovin, které jsou v procesu (nedokončená výroba čili NV) mají být zaúčtovány do hlavní knihy.

Hodnota surovin, které jsou ve zpracování (NV) se zaúčtuje na účty **Odhadované náklady na spotřebovaný materiál** a **Odhadované náklady na spotřebovaný materiál, NV**. Proces výdejky pro výrobní zakázku je fyzická aktualizace transakcí zásob souvisejících s výrobní zakázkou. Když je výrobní zakázka registrována jako ukončená, fyzické transakce jsou stornovány a související transakce zásob jsou finančně aktualizovány. Když je zaúčtován závěrečný deník, používají se typy zaúčtování **Spotřebované náklady na materiál** a **Spotřebované náklady na materiál, NV**.

Karta **Výroba** na stránce **Profily zaúčtování zásob** se používá k řízení toho, jak se výrobní zakázky zaúčtují do hlavní knihy. To se používá, když je pole **Zaúčtování do HK** nastaveno na **Zboží a prostředek** nebo **Zboží a kategorie** na stránce **Parametry modulu Řízení výroby**. 

Pro zaúčtování deníku výdejek pro výrobní zakázku do hlavní knihy musejí být splněny následující podmínky:

-   Na stránce **Parametry modulu Řízení výroby** musí být zaškrtnuto políčko **Zaúčtovat výdejku do hl. knihy**. Toto nastavení lze přepsat pro konkrétní web na stránce **Parametry modulu Řízení výroby podle pracoviště**.
-   Na stránce **Skupiny modelů položek** musí být pro položku vybranou na řádku nákupní objednávky zaškrtnuto políčko **Zaúčtovat fyzické zásoby**.
-   Hlavní účet musí být uvedený na stránce **Profil účtování zásob** pro následující typy zaúčtování:
    -   **Odhadované náklady na spotřebovaný materiál**
    -   **Odhadované náklady na spotřebovaný materiál, NV**

## <a name="time-consumption"></a>Spotřeba času

Čas, který pracovníci stráví na výrobních úlohách, je zaznamenán v **Deníku karet postupů** nebo **Deníku úkolových lístků**. Když tyto deníky jsou zaúčtovány, účtování hlavní knihy do vyhrazeného účtu pro prostředky, které jsou ve výrobě (NV). Toto zaúčtování představuje hodnota času stráveného na výrobní zakázce. Poté, co je výrobní zakázka registrována jako dokončená, jsou vyrovnány účty nedokončené výroby.

Existují tři možné způsoby, jak zaúčtovat spotřebu času v závislosti na možnosti vybrané v poli **Zaúčtování hlavní knihy** na stránce **Parametry modulu Řízení výroby**.

## <a name="reporting-finished-goods-and-error-quantities"></a>Hlášení dokončeného zboží a množství chyb

Je-li výrobní zakázka **Ohlášena jako dokončená**, jsou v zásobách aktualizována množství dokončeného zboží prostřednictvím **Deníku dokončené výroby**. Pokud používáte účtování NV, deník hlavní knihy se zaúčtuje a sníží tak účty NV a zvýší zásoby dokončeného zboží. Deník používá standardní náklady, které byly pro produkt definovány. Pokud je vybrána možnost **Použít odhadovanou nákladovou cenu** na stránce **Parametry modulu Řízení výroby**, budou použity odhadované náklady z výrobní zakázky.

Hodnota surovin, které jsou ve zpracování (NV) se zaúčtuje na účty **Odhadované výrobní náklady** a **Odhadované výrobní náklady, NV**. Proces **Oznámit jako dokončené** pro výrobní zakázku je fyzická aktualizace transakcí zásob souvisejících s výrobní zakázkou. Když je výrobní zakázka ukončena, fyzické transakce jsou stornovány a související transakce zásob jsou finančně aktualizovány. Když je zaúčtován závěrečný deník, používají se typy zaúčtování **Výrobní náklady** a **Výrobní náklady, NV**.

Karta **Výroba** na stránce **Profily zaúčtování zásob** se používá ke kontrole toho, jak se výrobní zakázky zaúčtují do hlavní knihy. To se používá, když je pole **Zaúčtování do HK** nastaveno na **Zboží a prostředek** nebo **Zboží a kategorie** na stránce **Parametry modulu Řízení výroby**. Pevnou záložku **Hlavní kniha – položky** na stránce **Výrobní skupiny** lze také použít k řízení účtování u výrobních zakázek, když je pole nastaveno na **Skupiny účtování výroby**.

Pro zaúčtování deníku **Oznámit jako dokončené** pro výrobní zakázku do hlavní knihy musejí být splněny následující podmínky:
-   Na stránce **Parametry modulu Řízení výroby** musí být zaškrtnuto políčko **Zaúčtovat dokončenou výrobu do hlavní knihy**. Toto nastavení lze přepsat pro konkrétní web na stránce **Parametry modulu Řízení výroby podle pracoviště**.
-   Na stránce **Skupiny modelů položek** musí být pro položku vybranou na řádku nákupní objednávky zaškrtnuto políčko **Zaúčtovat fyzické zásoby**.
-   Hlavní účet musí být uvedený na stránce **Profil účtování zásob** pro následující typy zaúčtování:
    -   **Odhadované výrobní náklady**
    -   **Odhadované výrobní náklady, NV**

## <a name="ending-the-production-order"></a>Ukončení výrobní zakázky

Před dokončením výrobní zakázky jsou vypočteny skutečné náklady pro vyrobené množství. Všechny odhadované náklady na materiál, práci a režii jsou stornovány a nahrazeny skutečnými náklady. Celkové náklady na dokončenou položku se zapíší na stranu MD účtu **Výrobní náklady** a na stranu Dal účtu **Výrobní náklady, NV**. Materiály, které byly spotřebovány během výrobní zakázky, se zapíší na stranu MD účtu **Spotřebované náklady na materiál** a na stranu Dal účtu **Náklady na materiál, NV**.

Pokud při spuštění výpočtu nákladů zaškrtnete políčko **Koncová práce**, bude stav výrobní zakázky změněn na **Ukončeno**. Nastavení tohoto stavu zabrání tomu, aby k dokončené výrobní zakázce byly nechtěně zaúčtovány další náklady. Můžete určit, že hodnota množství chyb, které jsou hlášeny jako dokončené, by měla být přidělena správným množstvím, která jsou hlášena jako dokončená. Zadáte také, že hodnota množství chyb bude účtována do vyhrazeného účtu odpadu. 

Pokud chcete nastavit konkrétní účet odpadu, postupujte následovně:
1.  Přejděte na **Řízení výroby** > **Nastavení** > **Parametry modulu Řízení výroby**.
2.  Vyberte kartu **Standardní aktualizace**.
3.  V poli **Metoda odpadu** vyberte **Účet odpadu**.
4.  V poli **Účet odpadu** vyberte hlavní účet, kam má být zaúčtován odpad v chybovém množství při ukončení výrobní zakázky. Vyberte například účet výdajů, jako je 510380: Výrobní odpad.

Pro zaúčtování závěrečného deníku pro výrobní zakázku do hlavní knihy musejí být splněny následující podmínky:
-   Hlavní účet musí být uveden na stránce **Profil účtování zásob** nebo **Výrobní skupiny** pro následující typy zaúčtování:
    -   **Spotřebované náklady na materiál**
    -   **Spotřebované náklady na materiál, NV**
    -   **Výrobní náklady**
    -   **Výrobní náklady, NV**
-   Hlavní účty musejí být uvedeny na stránce **Nákladové kategorie**, **Zdroje** nebo **Skupiny zdrojů** pro následující typy:
    -   **Absorbované výrobní náklady**
    -   **Spotřebované výrobní náklady, NV**

## <a name="indirect-costs-for-production-orders"></a>Nepřímé náklady na výrobní zakázky

Když zpracováváte transakce pro výrobní zakázku, můžete konfigurovat nepřímé náklady tak, aby zachycovaly režijní náklady nebo dodatečné poplatky ve vaší hlavní knize. Fyzické transakce pro nepřímé náklady se zaúčtují do zásob, když zaúčtujete deník výdejek nebo sestavu jako hotový deník. Finanční transakce pro nepřímé náklady se zaúčtují do zásob, když zaúčtujete závěrečný deník.

Nepřímé náklady uznáváte ve vaší spotřebě času související s deníky **Karta postupu** nebo **Karta úlohy**. Když dokončíte výrobní zakázku, jsou tyto transakce stornovány a zaúčtovány na finanční účty. Další informace naleznete v tématu [Nákladové formuláře](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Řízení úrovně účtování do hlavní knihy

Na stránce **Parametry modulu řízení výroby** lze použít pole **Zaúčtování do hlavní knihy** pro nastavení úrovně zaúčtování do hlavní knihy pro výrobní procesy. 

K dispozici jsou následující pole:

### <a name="item-and-resource"></a>Zboží a prostředek

Když vyberete možnost **Zboží a prostředek** v poli **Účtování v hlavní knize** pole, účetní účty pocházejí ze zdroje nebo skupiny zdrojů při operaci na trase. Účty na konkrétním zdroji budou první možností zaúčtování. Pokud není zadán účet, použijí se účty zadané ve skupině prostředků. Každý řádek operace na trase může mít jeden zdroj specifikovaný jako **Prostředek výpočtu nákladů**. Tento zdroj se používá k určení účtu, který se má použít. Tato možnost se běžně používá, když organizace k prostředkům přiřazuje provozní náklady. Náklady na zdroje jsou často vyšší a používají se k rozhodování typu „vyrobit versus koupit“. Toto je nejpodrobnější konfigurace účtování a umožňuje nejpodrobnější kontrolu účtování a velmi podrobnou analýzu výrobního procesu.

### <a name="item-and-category"></a>Zboží a kategorie

Když vyberete možnost **Zboží a kategorie** v poli **Účtování v hlavní knize**, budou účetní účty pocházet ze stránky **Kategorie nákladů** související s každým řádkem na trase. Každý řádek operace na trase může mít tři kategorie nákladů: čas **Nastavení**, čas **Spuštění** a **Množství**. Tato možnost se běžně používá, když se vaše organizace zaměřuje především na efektivitu procesů a trvání aktivity. Tato možnost představuje souhrnnější způsob účtování a stále poskytuje způsob, jak seskupit náklady do kategorií.

### <a name="production-group"></a>Skupina účtování výroby

Když vyberete možnost **Výrobní skupiny** v poli **Účtování v hlavní knize**, účty pro zaúčtování pocházejí ze stránky **Výrobní skupiny**. **Výrobní skupiny** se obvykle používají, když více než jedna výrobní linka vyrábí podobné produkty nebo má podobné vybavení. Tuto možnost můžete použít k porovnání nákladů mezi dvěma různými výrobními skupinami.  
  
> [!NOTE]
> Jestliže je použita standardní metoda výpočtu nákladů na dokončenou položku, projeví se tento fakt i ve výsledných transakcích. Jestliže je rozdíl mezi skutečnými náklady a náklady vypočtenými standardní metodou, rozdíly se zaúčtují na účet vykazující zisk nebo ztrátu.

### <a name="route-groups-and-ledger-posting"></a>Skupiny postupů a účtování do hlavní knihy

Každá provozní linka v postupu má určenou **Skupinu postupů**. Pole **Přípravný čas**, **Operační čas** a **Množství** v části **Skupina postupů** ve skupině **Odhad a výpočet nákladů** se používají ke kontrole, zda bude čas použit pro kalkulaci při účtování **Pracovní karty** nebo **Deníku karet postupů** na výrobní zakázce. Pokud jsou možnosti deaktivovány, nevytvoří se doklad spotřeby času v hlavní knize.

Pro zaúčtování **Karty postupu** nebo **Deníku úkolových lístků** pro výrobní zakázku do hlavní knihy musejí být splněny následující podmínky:

-   Pole **Přípravný čas**, **Operační čas** nebo **Množství** musí být vybráno ve skupině **Odhad a výpočet nákladů** na stránce **Skupina postupů**.
-   Hlavní účet musí být uveden na stránce **Nákladová kategorie**, **Postup**, **Skupina postupů** nebo **Výrobní skupiny** pro následující typy zaúčtování:
    -   Absorbované odhadované výrobní náklady
    -   Spotřebované odhadované výrobní náklady, NV

Následující diagram ukazuje vztah skupiny postupů k výpočtu celkových nákladů na každou operaci (linku postupu) v daném postupu. Každá linka postupu má jednu skupinu postupů. Skupina postupů řídí parametry pro přípravný čas, operační čas a množství. Karta **Nákladová kategorie** má tři možnosti **Příprava**, **Spuštění** a **Množství**, které jsou povoleny na základě nastavení skupin postupů. Pevná záložka **Časování** má tři pole, která jsou založena na skupině postupů.

Použitý vzorec je založen na tom, zda je tato možnost povolena ve skupině postupů. Náklady z vybrané kategorie nákladů se vynásobí množstvím, které bylo zadáno v časování, a výsledkem jsou celkové náklady.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Vztah skupin tras postupů k celkovým kalkulovaným nákladům.":::
Vztah skupin tras postupů k celkovým kalkulovaným nákladům. Každá linka postupu má jednu skupinu postupů. Skupina postupů řídí parametry pro přípravný čas, operační čas a množství. Karta Nákladová kategorie má tři možnosti Příprava, Spuštění a Množství, které jsou povoleny na základě nastavení skupin postupů. Pevná záložka Časování má tři pole, která jsou povolena a vypočítána na základě skupiny postupů. Použitý vzorec je založen na tom, zda je tato možnost povolena ve skupině postupů. Náklady z vybrané kategorie nákladů se vynásobí množstvím, které je zadáno v časování, a výsledkem jsou celkové náklady.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Ukázka konfigurace profilu zveřejňování

Následující tabulka ukazuje příklady výchozích typů účtování s ukázkovými hlavními účty a popisy. 

 - Sloupec **Má dáti / dal** označuje, zda lze účtovat transakce obvykle Má dáti nebo Dal nebo v některých případech obojí. 
 - Sloupec **Clearingový účet** označuje, zda typ účtování je clearingový účet. Částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce. 
 - Sloupec **P/F** označuje **P** pro fyzické zaúčtování a **F** pro finanční zaúčtování. 
 - Sloupec **Sledovat** udává, zda je hlavní účet pro určitý typ účtování obvykle stejný jako jiný typ účtování. Hodnota ve sloupci označuje typ účtování, který se obvykle sleduje.

> [!NOTE]
> Navrhované hlavní účty a názvy hlavních účtů jsou pouze návrhy. Doporučujeme, abyste ve spolupráci se svým účetním určili nejlepší konfiguraci pro vaše obchodní potřeby.


| Typ zaúčtování  | Příklad hlavního účtu | Příklad názvu hlavního účtu| Typ účtu | Má dáti/Dal? | Clearingový účet | Fyzická nebo finanční | Sledovat | Popis |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Odhadované náklady na spotřebovaný materiál      | 140100               | Zásoby materiálů        | Materiál        | Kredit         | Y                | P                     | Spotřebované náklady na materiál                | Tento účet se používá při zaúčtování deníku výdejek pro výrobní zakázku. Protiúčtem jsou Odhadované náklady na spotřebovaný materiál, NV. Částka zaúčtovaná na tomto účtu je automaticky stornována při dokončení výrobní zakázky. Tento účet představuje účet zásob v rozvaze.       |
| Odhadované náklady na spotřebovaný materiál, NV | 150150               | Výroba NV – Materiály | Materiál        | Debet          | Y                | P                     | Odhadované výrobní náklady, NV          | Tento účet se používá při zaúčtování deníku výdejek pro výrobní zakázku. Protiúčtem jsou Odhadované náklady na spotřebovaný materiál. Částka zaúčtovaná na tomto účtu je automaticky stornována při dokončení výrobní zakázky. Tento účet představuje NV ve vaší rozvaze.                  |
| Odhadované výrobní náklady               | 140200               | Zásoby dokončeného zboží   | Materiál        | Debet          | Y                | P                     | Výrobní náklady                         | Tento účet se používá při zaúčtování sestavy jako dokončeného deníku pro výrobní zakázku. Protiúčtem jsou Odhadované výrobní náklady, NV. Částka zaúčtovaná na tomto účtu je automaticky stornována při dokončení výrobní zakázky. Tento účet představuje účet zásob v rozvaze. |
| Odhadované výrobní náklady, NV          | 150150               | Výroba NV – Materiály | Materiál        | Kredit         | Y                | P                     | Výrobní náklady, NV                    | Tento účet se používá při zaúčtování sestavy jako dokončeného deníku pro výrobní zakázku. Protiúčtem jsou Odhadované výrobní náklady. Částka zaúčtovaná na tomto účtu je automaticky stornována při dokončení výrobní zakázky. Tento účet představuje NV ve vaší rozvaze.                     |
| Spotřebované náklady na materiál                | 140100               | Zásoby materiálů        | Materiál        | Kredit         | N                 | F                     | Odhadované náklady na spotřebovaný materiál      | Tento účet se používá k uznání materiálů, které jsou spotřebovány ve výrobní zakázce během ukončovacího procesu. Protiúčtem jsou Spotřebované náklady na materiál, NV.                                                                                                    |
| Spotřebované náklady na materiál, NV           | 150150               | Výroba NV – Materiály | Materiál        | Debet          | N                 | F                     | Odhadované náklady na spotřebovaný materiál, NV | Tento účet se používá k uznání materiálů v NV, které jsou spotřebovány ve výrobní zakázce během ukončovacího procesu. Protiúčtem jsou Spotřebované náklady na materiál.                                                |
| Výrobní náklady                         | 140200               | Zásoby dokončeného zboží   | Materiál        | Debet          | N                 | F                     | Odhadované výrobní náklady               | Tento účet se používá k uznání nákladů na hotové zboží, které je vyrobeno na základě výrobní zakázky, když výrobní zakázku ukončíte. Protiúčtem jsou Výrobní náklady, NV.                                                                  |
| Výrobní náklady, NV                    | 150150               | Výroba NV – Materiály | Materiál        | Kredit         | N                 | F                     | Odhadované výrobní náklady, NV          | Tento účet se používá k uznání nákladů na hotové zboží v NV, které je vyrobeno na základě výrobní zakázky, když výrobní zakázku ukončíte. Protiúčtem jsou Výrobní náklady.                                     |

> [!NOTE]
> **Příjem NV štíhlé služby** a **Clearing NV štíhlé služby** se používají u zpětného účtování nákladů pro štíhlou výrobu. Další informace naleznete v tématu [Zpětné účtování nákladů](/supply-chain/cost-management/backflush-costing.md).

