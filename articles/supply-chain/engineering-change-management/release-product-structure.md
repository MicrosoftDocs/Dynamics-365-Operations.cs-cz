---
title: Uvolnění struktur produktu
description: Toto téma vysvětluje, jak můžete kromě uvolnění produktů společně s jejich technickými verzemi uvolnit kompletní produktové struktury. Tímto způsobem můžete zajistit, že technicky relevantní data o produktech lze snadno znovu použít v různých právnických osobách.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c1304d3277e12bc602fa5bc25a61e1f95edba59c
ms.sourcegitcommit: 4835acc3edacf8277937723d3f85a7875bd8de83
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/11/2021
ms.locfileid: "5580908"
---
# <a name="release-product-structures"></a>Uvolnění struktur produktu

[!include [banner](../includes/banner.md)]

Aby bylo zajištěno, že technicky relevantní data produktu lze snadno znovu použít v různých právnických osobách, můžete kromě uvolnění produktů společně s jejich technickými verzemi uvolnit i kompletní produktové struktury. Proto můžete v rámci jedné akce uvolnění struktur uvolnit víceúrovňové kusovníky společně s nadřazenou položkou. V tomto případě se uvolní také kusovník a produkty nižší úrovně.

Technické produkty jsou vytvářeny a udržovány jejich technickou společností takovým způsobem, aby splňovaly požadavky na kvalitu již při jejich navrhování. Každá provozní společnost, která vyrábí produkt, potřebuje stejný produkt a základní kusovník. V závislosti na produkčním zařízení může být postup vytvořen místně. V takovém případě neuvolníte postup společně s produktem. U právnických osob, které budou produkty prodávat, ale nebudou je vyrábět, nemusí být kusovník vyžadován.

Aby byl proces efektivnější, mohou být všechna technicky relevantní data současně poskytována dalším provozním společnostem. Tato data zahrnují strukturu produktu. Během procesu uvolnění si můžete vybrat, která část údajů o produktu má být uvolněna.

Další informace o technických a provozních společnostech viz [Technické společnosti a pravidla vlastnictví dat](engineering-org-data-ownership-rules.md).

Všimněte si, že můžete uvolnit jak standardní produkty, tak technické produkty společně s uvolněním struktury produktu. Během tohoto procesu bude uvolněna celá struktura produktu, dokonce i kusovník a postup ze společnosti, ve které jsou produkty uvolňovány.

Příklad uvolnění produktu najdete v části [Uvolnění technického produktu do místní společnosti](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Uvolněná data produktu, když se použije uvolnění struktury produktu

V uvolnění technických produktů jsou zahrnuty následující údaje:

- **Data produktu** - Je vytvořen nový uvolněný produkt.
- **Data technické verze** - Technická verze a její data jsou vytvořena nebo aktualizována. Všimněte si, že pokud znovu uvolníte stejnou technickou verzi do provozní společnosti, budou technická data přepsána.
- **Technické atributy** - Technické atributy a jejich hodnoty jsou vytvářeny nebo aktualizovány.
- **Technické kusovníky** - Technický kusovník a jeho řádky lze vytvářet nebo aktualizovat. Další informace o vlastnictví dat získáte v části [Vlastníci produktu](product-owner.md).
- **Technické postupy** - Technické postupy a jejich operace lze vytvářet nebo aktualizovat. Další informace o vlastnictví dat získáte v části [Vlastníci produktu](product-owner.md).
- **Technické dokumenty** - Technické dokumenty, které jsou připojeny k technické verzi, jsou vytvořeny nebo aktualizovány.

Když ve svém systému zapnete správu technických změn, je k dispozici struktura produktu uvolnění. Kromě toho budou standardní produkty po uvolnění obsahovat jejich kusovníky a postupy.

## <a name="product-acceptance"></a>Přijetí produktu

**Přijetí produktu** je klíčový parametr, který ovlivňuje proces uvolnění. Tento parametr můžete nastavit pro každou společnost tak, že přejdete na **Správa technických změn \> Nastavení \> Parametry správy technických změn**. Další informace naleznete v tématu [Parametry správy technických změn](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Automatické přijetí produktu

Každé vydání technických produktů začíná, když si někdo z technické společnosti vybere produkt k uvolnění. Když je parametr **Přijetí produktu** nastaven na *Automatický*, uživatel v technické společnosti rozhodne, která produktová data by měla být automaticky uvolněna do provozních společností. Produkt bude poté automaticky uvolněn do společností vybraných v průvodci uvolněním.

### <a name="manual-product-acceptance"></a>Ruční přijetí produktu

Každé vydání technických produktů začíná, když si někdo z technické společnosti vybere produkt k uvolnění. Když je parametr **Přijetí produktu** nastaven na *Ruční*, uživatel v technické společnosti rozhodne, která produktová data by měla být ručně uvolněna do provozních společností. Uživatel z každé provozní společnosti poté zkontroluje produktová data a rozhodne, zda uvolnění přijme. Uživatel v provozní společnosti může při přijetí dat nastavit následující možnosti:

- Pokud produkty (aktualizace) nejsou relevantní pro provozní společnost, může se uživatel rozhodnout uvolnění nepřijmout.
- Uživatel může změnit šablonu položky pro nové produkty.
- Uživatel si může vybrat, zda má být produkt vydán společně s jejich kusovníky anebo postupy a zda má být uvolněn jako schválený a aktivní.
- Uživatel může změnit data účinnosti produktů.

Příklad toho, jak produkt přijmout, najdete v části [Než produkt vydáte v místní společnosti, zkontrolujte jej a přijměte](engineering-scenarios.md#accept).

> [!NOTE]
> U standardních produktů můžete uvolnit z jakékoli právnické osoby do jakékoli jiné právnické osoby. U technických produktů je jedinou právnickou osobou, ze které můžete uvolnit, technická společnost.

## <a name="release-policies"></a>Zásady uvolnění

Ne všechny provozní společnosti potřebují stejná produktová data. Obecně platí, že provozní společnosti, které vyrábějí technické výrobky, vyžadují kusovník, zatímco provozní společnost, která prodává pouze technické výrobky, kusovník nevyžadují. Zásady uvolnění můžete použít k určení parametrů, které se používají k uvolnění produktů.

Další informace o kategoriích technických produktů najdete v části [Technické verze a kategorie technických produktů](engineering-versions-product-category.md).

Během procesu uvolnění můžete ovlivnit nastavení.

## <a name="create-and-manage-product-release-policies"></a>Vytváření a správa zásad uvolnění produktu

Chcete-li pracovat se zásadami uvolnění produktu, přejděte na **Správa technických změn \> Nastavení \> Zásady uvolnění produktu**. Potom proveďte jeden z následujících kroků.

- Chcete-li vytvořit novou zásadu, vyberte **Nová** v podokně akcí a poté nastavte pole, jak je popsáno v následujících podsekcích.
- Chcete-li upravit existující zásadu, vyberte ji v podokně seznamu, zvolte **Upravit** v podokně akcí a poté nastavte pole, jak je popsáno v následujících podsekcích.
- Chcete-li odstranit existující zásadu, vyberte ji v podokně seznamu a vyberte **Upravit** v podokně akcí a poté se na záložce s náhledem **Obecné** ujistěte, že možnost **Aktivní** je nastavena na *Ne*. Poté v podokně akcí zvolte **Odstranit**.

### <a name="header"></a>Záhlaví

V záhlaví zásad uvolnění produktu nastavte následující pole.

| Pole | popis |
|---|---|
| Jméno | Zadejte název zásady. |
| popis | Zadejte popis zásady. |

### <a name="general-fasttab"></a>Záložka s náhledem Obecné

Na záložce s náhledem **Obecné** zásad uvolnění produktu nastavte následující pole.

| Pole | popis |
|---|---|
| Typ produktu | Vyberte, zda se zásada vztahuje na produkty typu *Položka* nebo *Služba*. Po uložení záznamu toto nastavení nemůžete změnit. |
| Použít šablony | Vyberte jednu z následujících možností a určete, zda a jak mají být šablony uvolnění produktu použity, když se použije zásada:<ul><li>**Vždy** - Pro uvolnění musí být vždy použit produkt uvolněný pomocí šablony. Pokud vyberete tuto možnost, použijte záložku s náhledem **Všechny produkty** k určení šablony, která se používá pro každou společnost, do které uvolňujete Pokud nezadáte šablonu pro každou společnost, která je uvedena na záložce s náhledem **Všechny produkty**, při pokusu o uložení této zásady se zobrazí chyba.</li><li>**Volitelné** - Pokud je produkt uvolněný pomocí šablony uveden pro společnost uvedenou na záložce s náhledem **Všechny produkty**, tato šablona bude použita při uvolnění do této společnosti. Jinak nebude použita žádná šablona. Pokud vyberete tuto možnost, můžete zásadu uložit bez přiřazení šablon všem společnostem. (Nezobrazí se žádné varování.)</li><li>**Nikdy** - Pro společnosti, do kterých uvolníte, nebude použit žádný produkt vydaný pomocí šablony, a to ani v případě, že je zadána šablona pro společnosti uvedené na záložce s náhledem **Všechny produkty**. Sloupce šablony nebudou k dispozici.</li></ul> |
| Aktivní | Pomocí této možnosti můžete zachovat zásady uvolnění. Nastavte možnost na *Ano* pro všechny zásady uvolnění, které používáte. Nastavte ji na *Ne*, čímž označíte zásadu uvolnění jako neaktivní, když se nepoužívá. Všimněte si, že nemůžete deaktivovat zásadu uvolnění, která je přiřazena kategorii technického produktu, a můžete odstranit pouze neaktivní zásady uvolnění. |

### <a name="all-products-fasttab"></a>Záložka s náhledem Všechny produkty

Na záložce s náhledem **Všechny produkty** přidejte řádek pro každou provozní společnost, do které uvolňujete a pro kterou chcete tuto zásadu použít. Pomocí tlačítek na záložce s náhledem **Všechny produkty** můžete podle potřeby přidávat a odebírat řádky. Pro každý řádek, který přidáte, nastavte následující pole.

> [!NOTE]
> Nastavení na záložce s náhledem **Všechny produkty** platí jak pro technické výrobky, tak pro standardní výrobky.

| Pole | popis |
|---|---|
| ID účtů společnosti | Vyberte společnost, na kterou se řádek vztahuje. Parametry na řádku se použijí při uvolnění produktů do této společnosti. |
| Šablona uvolněného produktu | Přidejte šablonu pro produkt. |
| Kopírovat schválení kusovníku | Zaškrtnutím tohoto políčka zkopírujete stav schválení kusovníku do přijímající společnosti. |
| Kopírovat aktivaci kusovníku | Zaškrtnutím tohoto políčka zkopírujete stav aktivace kusovníku do přijímající společnosti. |
| Kopírovat schválení postupu | Zaškrtnutím tohoto políčka zkopírujete stav schválení postupu do přijímající společnosti.|
| Kopírovat aktivaci postupu | Zaškrtnutím tohoto políčka zkopírujete stav aktivace postupu do přijímající společnosti. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Záložka s náhledem Parametry volby pro technické produkty

Pokaždé, když přidáte řádek na záložce s náhledem **Všechny produkty**, řádek, který má odpovídající hodnotu **ID firemních účtů** se vytvoří také na záložce s náhledem **Parametry volby pro technické produkty**. Poté když odstraníte řádek ze záložky s náhledem **Všechny produkty**, řádek, který má odpovídající hodnotu **ID firemních účtů** se odstraní také ze záložky s náhledem **Parametry volby pro technické produkty**.

Pro každý řádek, který je zobrazen na záložce s náhledem **Parametry volby pro technické produkty**, nastavte následující pole.

> [!NOTE]
> Nastavení na záložce s náhledem **Parametry volby pro technické produkty** platí pouze pro technické produkty.

| Pole | popis |
|---|---|
| Šablona kusovníku | Po vydání produktu, který má kusovník, budou přidány řádky specifikovaného kusovníku šablony. Toto pole je užitečné pro přidání místních komponent, jako je balení nebo pokyny v místním jazyce. |
| Postup šablony | Po vydání produktu, který má postup, budou přidány řádky specifikované šablony. |
| Kopírovat platnost | Vyberte, zda mají být data platnosti zkopírována z technické společnosti do provozní společnosti, když uvolňujete produkty. |
| Automaticky přidat do návrhu uvolnění | Zaškrtněte toto políčko u produktů, které by měly být automaticky uvolněny v příkazu k technických změnám. Tímto způsobem mohou být produkty, které patří do kategorií technických produktů používajících tuto zásadu uvolnění, automaticky uvolněny do provozních společností, kde je tato možnost nastavena. (Další informace naleznete v tématu [Správa změn technických produktů](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Po uvolnění zkontrolujte každý produkt

Když budou uvolněny technické produkty, které mají kusovníky nebo postupy, budou parametry nastaveny na výchozí hodnoty, jak je uvedeno v zásadách uvolnění. Jako uživatel můžete toto chování ovlivnit na straně uvolnění, když použijete uvolnění struktury produktu.

Chcete-li uvolnit technické produkty, na stránce **Uvolněné produkty** vyberte produkty, které chcete uvolnit, a poté vyberte **Uvolnění struktury produktu** pro otevření průvodce uvolněním. Stránka **Vybrat technické produkty k uvolnění** zobrazuje produkty. Vyberte jeden produkt a poté vyberte **Podrobnosti uvolnění** pro kontrolu podrobností uvolnění produktu.

Na stránce **Podrobnosti uvolnění** můžete změnit hodnotu polí **Přijmout kusovník**, **Kopírovat schválení kusovníku**, **Kopírovat aktivaci kusovníku**, **Přijmout kusovník**, **Kopírovat schválení postupu** a **Kopírovat aktivaci postupu**. Ve scénáři push-pull můžete změnit hodnotu stejných polí na přijímací straně za předpokladu, že jsou uvolněny kusovník a postup.

## <a name="product-owners-and-product-releases"></a>Vlastníci produktů a uvolnění produktů

Protože vlastníci produktů vědí, které právnické osoby jejich produkty potřebují, produkt mohou uvolnit pouze členové skupiny vlastníků produktů daného produktu. Ostatní uživatelé nemohou uvolňovat produkty, které nevlastní.

Toto chování platí pouze v případě, že je produkt přímo vybrán k uvolnění. Produkty, které jsou součástí struktury jiného produktu prostřednictvím kusovníku *mohou* být uvolněny uživateli, kteří nejsou vlastníky, když uvolňují nadřazený produkt za předpokladu, že nadřazený produkt vlastní.

Například produkt X je přiřazen ke skupině vlastníků produktu *Designové skříňky*. Produkt X je také součástí kusovníku produktu Y, který je přiřazen ke skupině vlastníků produktů *Designové reproduktory*. Pokud uživatel ze skupiny vlastníků produktů *Designové reproduktory* uvolňuje produkt Y a jeho kusovník, produkt X bude uvolněn společně s produktem Y.

Další informace naleznete v tématu [Vlastníci produktů](product-owner.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
