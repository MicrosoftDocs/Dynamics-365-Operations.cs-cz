---
title: Časté otázky týkající se výpočtu nákladů zásob
description: Tento článek poskytuje odpovědi na časté otázky týkající se výpočtu nákladů na zásoby v Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 5a1d86e7e9cca159d0a820680714a08dc73c0688
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068386"
---
# <a name="inventory-costing-faq"></a>Časté otázky týkající se výpočtu nákladů zásob

[!include [banner](../includes/banner.md)]

Tento článek poskytuje odpovědi na časté otázky týkající se výpočtu nákladů na zásoby v Microsoft Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Uzávěrka skladu, vyrovnání a přepočet

### <a name="is-the-inventory-close-required"></a>Je nutná uzávěrka zásob?

Pokud plánujete používat funkci archivace zásob, je nutná uzávěrka zásob. Pokud neplánujete používat funkci archivace zásob, důrazně doporučujeme, abyste přesto spustili uzávěrku zásob, bez ohledu na modely výpočtu nákladů, které používáte.

### <a name="how-often-should-the-inventory-close-be-run"></a>Jak často by měla být prováděna uzávěrka zásob?

Uzávěrka zásob by měla být provedena alespoň jednou za účetní období. Pokud je například vaše účetní kniha nastavena na fiskální kalendář založený na kalendářním měsíci, měli byste provést uzávěrku zásob jednou za měsíc.

### <a name="is-the-inventory-recalculation-required"></a>Je nutná rekalkulace zásob?

Ne, rekalkulace zásob se nevyžaduje. Pokud používáte periodický model výpočtu nákladů, jako je první do skladu, první ven (FIFO), poslední do skladu, první ven (LIFO) nebo vážený průměr, měli byste pečlivě zvážit, zda spustíte přepočet zásob. Může poskytnout přesnější výpočet nákladů v heuristických modelech, které jste vybrali.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Jak často by měla být prováděna rekalkulace zásob?

Pokud plánujete spustit přepočet zásob, doporučujeme zvážit jeho každodenní spouštění jako dávkový proces. Pokud vaše organizace nevyžaduje časté vykazování hodnot zásob pro modely periodických výpočtů nákladů, můžete zvážit spouštění kalkulace zásob méně často.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Kdy mám použít vyrovnání zásob na skladě na stránce Uzávěrka a vyrovnání?

Vyrovnání zásob na skladě lze spoustit pouze po dokončení uzávěrky zásob. Obvykle se spouští pro datum po poslední uzávěrce. Okamžité vyrovnání může upravit pouze zásoby, které jsou stále na skladě k datu spuštění úpravy.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Kdy mám použít vyrovnání transakcí zásob na stránce Uzávěrka a vyrovnání?

Před spuštěním uzávěrky zásob byste měli použít vyrovnání transakcí zásob. Obvykle se používá k opravě nesprávného příjmu. Vyrovnání transakcí zásob nelze zaúčtovat po provedení uzávěrky zásob a vypořádání transakce.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Zachází se s vratkami nákupních objednávek jako s jinými výdeji během uzávěrky zásob?

Ano. Příjem nákupní objednávky je výdej, který se vypořádá s příjmem v heuristickém modelu, který vyberete pro položku. Pokud používáte model periodického výpočtu nákladů, můžete k přepsání heuristických nákladů použít označení.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Co se stane s vratkou prodejní objednávky během uzávěrky zásob?

Když spustíte uzávěrku zásob, je vratka prodejní objednávky považována za příjem do zásob. Výdeje se vypořádají proti zásobám na základě heuristického modelu, který pro položku vyberete.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Jaká nákladová cena se používá u vratky prodejní objednávky?

Když vytvoříte vratku, která souvisí s prodejní objednávkou, hodnota pole **Jednotková cena** se zkopíruje z původní prodejní objednávky a pole **Nákladová cena vrácení** na vratce je nastaveno na upravenou nákladovou cenu z původní transakce zásob pro řádek prodejní objednávky, který se vrací. Pokud je možnost **Hodnota otevřena** pro související transakci zásob nastavena na *Ano*, uzávěrka zásob může způsobit aktualizace nákladů na výdej původní prodejní objednávky. Pole **Nákladová cena vrácení** není v tomto scénáři aktualizováno. Když však odešlete dodací list objednávky vrácení, systém zkontroluje nákladovou cenu a použije aktualizované náklady na skladovou transakci vrácení.

Pro vratku položky standardních nákladů, která se vztahuje k prodejní objednávce, systém použije standardní náklady z doby původní prodejní objednávky, i když jsou pro položku aktivní nové standardní náklady.

Když vytvoříte vratku, která nesouvisí s prodejní objednávkou, pole **Nákladová cena vrácení** je nastaveno na cenu aktivní položky, kterou máte pro položku na místě, pro které vytváříte objednávku vratky. Pokud pro položku nemáte aktivní nákladovou cenu v nákladové verzi, bude hodnota 0 (nula). Pokud ponecháte hodnotu 0 (nula), obdržíte varování, že není zadané ID šarže vratky nebo nákladová cena vratky.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Jaký je očekávaný výkon uzávěrky zásob?

Výkon uzávěrky zásob může ovlivnit mnoho faktorů. Mezi tyto faktory patří celkový počet položek, celkový počet transakcí v období, modely zásob, které používáte, a počet pomocníků pro dávky, které konfigurujete v parametrech řízení zásob a skladu. Můžete očekávat, že uzávěrka může trvat od několika minut až po několik hodin. Neexistují žádné konkrétní pokyny ohledně doby, po kterou by uzávěrka měla trvat. Měli byste definovat své nefunkční obchodní požadavky na výkon uzávěrky zásob a úzce spolupracovat se svým partnerem na definování plánu spuštění procesu uzávěrky zásob. Pokud zaznamenáte neočekávaně nízký výkon procesu uzávěrky zásob, měli byste otevřít lístek podpory.

## <a name="costing-sheet-and-indirect-costs"></a>Nákladový formulář a nepřímé náklady

### <a name="which-costing-models-support-the-costing-sheet"></a>Které modely výpočtu nákladů podporují nákladový formulář?

Přestože se nákladový formulář nejčastěji používá v organizacích, které používají standardní výpočet nákladů, můžete jej použít s jakýmkoli modelem výpočtu nákladů, který je dostupný v Supply Chain Management.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Mohu mít více nákladových formulářů pro různé části mé organizace?

Číslo Na jednu právnickou osobu můžete mít pouze jeden nákladový formulář.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Mohu mít různé nákladové formuláře pro každé pracoviště?

Ne, nemůžete mít různé nákladové formuláře pro každé pracoviště. Na jednu právnickou osobu můžete vytvořit pouze jeden nákladový formulář. Můžete však nakonfigurovat celkové uzly, nákladové skupiny nebo nepřímé nákladové uzly pro každé pracoviště. Tato konfigurace je ruční proces a při organizačních nebo provozních změnách musíte udržovat hierarchii a přiřazení položek v nákladovém formuláři. Pokud je jedna položka vyrobena nebo zakoupena na více než jednom pracovišti, neexistuje žádný mechanismus, který by vám umožnil zacházet s položkou nákladového formuláře pro každé pracoviště odlišně. Kromě toho si uvědomte, že všechny kódy nepřímých nákladů mají sazbu nebo příplatek, který je definován ve vašem nákladovém formuláři. Náklady, které definujete, jsou vždy specifické pro dané pracoviště.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Mohu deaktivovat a aktivovat verze nákladového formuláře?

Přestože pro nákladový formulář není uchovávána žádná podrobná historie verzí, můžete v nákladovém formuláři provést změny a poté, až budete připraveni, jej uložit a ověřit. Neexistuje žádný mechanismus, který by vám umožnil vrátit se ke starší verzi nákladového formuláře nebo zobrazit změny provedené v nákladovém formuláři. Pokud zahájíte změny a nechcete, aby se projevily, můžete stránku zavřít bez uložení a ověření změn. Budete vyzváni ke zrušení změn.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Mohu vytvořit nepřímé náklady pro každou položku?

Ve svém nákladovém formuláři můžete vytvořit kódy nepřímých nákladů, kde je pole **Typ uzlu** nastaveno na *Příplatek*, *Sazbu* nebo *Na základě výstupní jednotky*. Potom můžete definovat sazbu nebo příplatek tak, aby byly specifické pro číslo položky. Na pevné záložce **Sazba** nebo **Příplatek** přidejte řádek do mřížky. Nastavte pole **Platný pro** na možnost *Tabulka* a pole **Vztah** na konkrétní číslo položky.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Mohu vytvořit nepřímé náklady, které nesouvisí s konkrétní položkou?

Ano. Můžete vytvořit kód nepřímých nákladů, kde je pole **Typ uzlu** nastaveno na *Na základě výstupní jednotky*. Poté můžete nastavit pole **Podtyp** na *Množství*, *Hmotnost* nebo *Objem* a zadat množství, hmotnost nebo objem položky, kterou vyrábíte. Sazba, kterou zadáte na pevné záložce **Sazba**, bude použita na podtyp, který jste vybrali. Například nastavíte pole **Podtyp** na *Množství* a pole **Sazba** na *1,00 USD* a poté vytvoříte výrobní nebo dávkovou objednávku pro množství 10. V tomto případě jsou nepřímé náklady, které budou přidány k hotovému zboží, 10,00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Mohu použít nákladový formulář k rozdělení svých výrobních nákladů podle hodin a materiálů?

Ano. Můžete vytvořit uzly **Celkem** ve vašem nákladovém formuláři k oddělení nákladů podle libovolného seskupení, které si vyberete. Můžete si ho například vytvořit jeden uzel **Celkem**, který je pojmenován *Hodiny* a další, který má název *Materiály*. Do uzlu **Hodiny** přidejte každou skupinu kódů, která souvisí s vašimi hodinami. Do uzlu **Materiály** přidejte každou skupinu nákladů, která souvisí s vašimi materiály.

## <a name="dimension-groups"></a>Skupiny dimenzí

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Mohu spravovat náklady na úrovni šarže nebo sériového čísla?

Ano, pokud používáte model periodických výpočtů nákladů, jako je FIFO, LIFO, datum LIFO, vážený průměr nebo datum váženého průměru, můžete povolit možnost **Finanční zásoby** pro dimenze **Šarže** nebo **Sériové číslo** ve skupině sledovacích dimenzí pro podrobné sledování nákladů.

### <a name="can-i-manage-costs-at-the-location-level"></a>Mohu spravovat náklady na úrovni umístění?

Ne, nemůžete povolit možnost **Finanční zásoby** pro dimenzi **Umístění** ve skupině dimenzí úložiště. Pokud vaše organizace musí sledovat náklady na podrobnější úrovni, zvažte, zda můžete vytvořit virtuální sklady, a poté vyberte možnost **Finanční zásoby** pro dimenzi **Sklad** ve vaší skupině dimenzí úložiště.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Měl bych povolit možnost Používat procesy řízení skladu pro skupinu dimenzí úložiště?

Pokud si myslíte, že byste v budoucnu mohli používat procesy správy skladu (WMS), měli byste povolit možnost **Používat procesy řízení skladu**. Po uložení skupiny dimenzí úložiště již pro ni nemůžete změnit nastavení možnosti **Používat procesy řízení skladu**. Pokud se později rozhodnete využít procesy řízení skladu, budete muset vytvořit nový sklad, kde je tato možnost povolena. Neexistuje žádný automatizovaný proces, který byste mohli použít k přesunu veškerých zásob z jednoho skladu do jiného skladu nebo ke kopírování souvisejících konfigurací do nového skladu.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-warehouse-management-processes-wms"></a>Mohu povolit Použití procesů správy skladu pro skupinu dimenzí úložiště, i když neplánuji používat procesy řízení skladu (WMS)?

Ano, i když neplánujete používat procesy správy skladu (WMS), můžete povolit možnost **Používat procesy řízení skladu** pro skupinu dimenzí úložiště. Chcete-li vytvořit a zpracovat transakce, budete muset dokončit minimální konfiguraci, jako jsou hierarchie rezervací a skupiny sekvencí jednotek. Nastavení WMS jsou však obecně ignorována, když ručně zpracováváte výdejky, dodací listy a příjemky produktů (například na stránkách prodejní objednávky a nákupní objednávky).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Kdy mám povolit možnost Fyzické zásoby pro skupinu dimenzí úložiště nebo sledování?

Měli byste povolit možnost **Fyzické zásoby** pro skupiny skladování a sledovacích dimenzí, když musíte vést podrobné záznamy zásob založené na této dimenzi. Obvykle bude každá aktivní dimenze také fyzicky sledována. Jakýkoli příjem, výdej nebo pohyb zásob tedy bude sledován podle zvolené dimenze. Pokud dimenze není povinná (například SPZ), můžete povolit možnost **Prázdný příjem povolen** a **Prázdný výdej povolen**, které uživatelům umožní přijímat, vydávat nebo přesouvat zásoby, i když dimenze není specifikována.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Kdy mám povolit možnost Finanční zásoby pro skupinu dimenzí úložiště nebo sledování?

Měli byste povolit možnost **Finanční zásoby** pro skupiny skladování a sledovacích dimenzí, když musíte vést podrobné finanční záznamy založené na této dimenzi. Dimenze **Pracoviště** jsou vždy finančně sledovány, zatímco ostatní dimenze jsou pro finanční sledování volitelné. Pokud používáte model periodických nákladů, jako je FIFO, LIFO nebo vážený průměr, povolením možnosti **Finanční zásoby** pro dimenzi označíte, že budete provádět vyúčtování pouze v případech, kdy příjem a výdej mají stejné hodnoty dimenzí. Pokud například povolíte možnost **Finanční zásoby** pro dimenzi **Sklad**, budete mít v každém skladu jiné náklady a příjemky a výdejky z různých skladů nelze vypořádat.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Mohu provést změny ve skupině dimenzí produktu, úložiště nebo sledování poté, co transakce existují?

Po vytvoření skupiny modelů položek můžete změnit nastavení polí **Plán disponibility podle dimenzí**, **Pro nákupní ceny** a **Pro prodejní ceny**, pokud je zaškrtnuto políčko **Aktivní** pro dimenzi ve skupině modelů položek. Žádné další změny nejsou povoleny. Nemůžete například povolit nebo zakázat možnosti **Aktivní**, **Povolen prázdný výdej**, **Povolen prázdný příjem**, **Fyzické zásoby** a **Finanční zásoby**.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Mohu změnit skupinu dimenzí produktu, úložiště nebo sledování pro uvolněný produkt?

Pokud jsou zásoby na skladě pro produkt 0 (nula) a možnost **Otevřená hodnota** je nastavena na *Ne* pro všechny transakce zásob, můžete změnit skupiny dimenzí úložiště a sledování na stránce uvolněného produktu. Po vytvoření záznamu již nelze změnit skupinu dimenzí produktu.

## <a name="item-model-groups"></a>Skupiny modelů položek

### <a name="when-should-i-enable-the-stocked-product-option"></a>Kdy mám aktivovat možnost Produkt na skladě?

Možnost **Produkt na skladě** byste měli povolit pro jakoukoli položku, která bude sledována ve vašich zásobách. Když je tato možnost povolena, uchovávají se podrobné transakce zásob, které sledují příjem a výdej položky. Tato možnost je obvykle povolena například pro jakoukoli hmotnou položku, kterou máte ve skladu. Tuto možnost byste také měli povolit, pokud plánujete přidat nehmotnou položku, jako je servisní položka, do kusovníků nebo vzorců. Pokud nepovolíte možnost **Produkt na skladě**, v dílčí knize zásob nejsou sledovány žádné transakce zásob a náklady na položky jsou obvykle účtovány do nákladů v hlavní knize. Tato možnost se často používá například pro zásoby obchodu nebo služby, které nejsou zahrnuty ve vašich kusovnících nebo vzorcích.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Kdy mám povolit možnost Zaúčtovat fyzické zásoby?

Možnost **Zaúčtovat fyzické zásoby** je obvykle povolena, když je povolena možnost **Produkt na skladě**. Když povolíte tuto možnost, systém bude sledovat fyzickou aktualizaci položky v transakci zásob. Tato možnost se používá v koordinaci s parametry v Závazcích, Pohledávkách a Řízení výroby, které určují, že fyzická aktualizace má vytvořit doklad. Tuto možnost obvykle povolíte, když chcete, aby se účetní kniha aktualizovala pokaždé, když fyzicky aktualizujete zásoby. Pokud Supply Chain Management není vaším systémem záznamů financí, možná budete chtít tuto možnost zakázat.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Kdy mám povolit možnost Zaúčtovat finanční zásoby?

Možnost **Zaúčtovat finanční zásoby** je obvykle povolena, když je povolena možnost **Produkt na skladě**. Tato možnost se používá v koordinaci s parametry v Závazcích, Pohledávkách a Řízení výroby, které určují, že finanční aktualizace má vytvořit doklad. Tuto možnost obvykle povolíte, když chcete, aby se účetní kniha aktualizovala při každé finanční aktualizaci zásob (například fakturací prodejních objednávek a nákupních objednávek nebo ukončením výrobní zakázky). Pokud Supply Chain Management není vaším systémem záznamů financí, možná budete chtít tuto možnost zakázat.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Kdy mám povolit možnost Zaúčtovat do odloženého účtu výnosů při dodání prodeje?

Možnost **Zaúčtovat do odloženého účtu výnosů při dodání prodeje** se používá k označení, zda chcete zaúčtovat výnosy v hlavní knize, když zaúčtujete dodací list pro prodejní objednávku. Tato možnost se obvykle používá, když máte dlouhou prodlevu mezi dodacím listem a fakturou na prodejní objednávce nebo když není možné fakturovat všechny prodejní objednávky v daném období. Obvykle tuto možnost zakážete, pokud zaúčtujete faktury prodejní objednávky ihned po zaúčtování dodacího listu. Tímto způsobem se vyhnete generování dalších účtování do hlavní knihy, která budou okamžitě stornována, když fakturujete prodejní objednávku.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Kdy mám povolit možnost Časově rozlišit pasiva na příjemce produktu?

Ve většině organizací budete chtít povolit možnost **Časově rozlišit pasiva na příjemce produktu** pro všechny skupiny modelů položek, bez ohledu na to, zda máte produkt na skladě, nebo produkt, který není na skladě. Tato možnost se používá k zaúčtování časového rozlišení do hlavní knihy na základě ceny příjmu produktu. Vzhledem k tomu, že obvykle dochází ke zpoždění mezi zaúčtováním příjmu produktu pro nákupní objednávku a zaúčtováním faktury, musí většina organizací zaúčtovat závazek v rozvaze, aby vyhověla místním předpisům, jako jsou obecně uznávané účetní postupy (GAAP). Pokud Supply Chain Management není vaším systémem záznamů financí, možná budete chtít tuto možnost zakázat. Pokud vaše organizace používá kategorie nákupu na nákupních objednávkách, můžete řídit požadavek na časové rozlišení povolením možnosti **Časově rozlišený nákupní výdaj na příjemce** pro pravidlo zásad kategorie na stránce **Zásady nákupu**.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Jak mohu uživateli zabránit zaúčtování příjmu produktu nákupní objednávky, pokud registrace příjmu ještě není zaúčtována?

Pokud ještě neproběhla registrace nákupní objednávky, můžete uživateli zabránit v zaúčtování příjmu produktu nákupní objednávky tím, že povolíte možnost **Požadavky na registraci** pro skupinu modelů položek. Tato možnost se obvykle používá v organizacích, které používají proces příjmu ve dvou krocích, nebo ve scénářích, kde musíte zaregistrovat číslo šarže nebo sériové číslo, například u položek, které přijímáte. Možnost **Požadavek na registraci** se vztahuje na *všechny* příjmy zásob pro položku, nejen pro nákupní objednávky. Například se vztahuje na deník zásob, který má kladné množství a výkaz výrobní zakázky jako hotový deník.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Jak mohu uživateli zabránit zaúčtování faktury nákupní objednávky, pokud příjem produktu ještě není zaúčtován?

Pokud ještě neproběhl příjem produktu nákupní objednávky, můžete uživateli zabránit v zaúčtování faktury produktu nákupní objednávky tím, že povolíte možnost **Požadavky na příjem** pro skupinu modelů položek. Tato možnost se obvykle používá v organizacích, které vyžadují, aby byly příjmy fyzicky rozpoznány v hlavní knize pro časová rozlišení. Možnost **Požadavek na příjem** se vztahuje na *všechny* příjmy zásob pro položku, nejen pro nákupní objednávky. Například se vztahuje na deník zásob, který má kladné množství a výkaz výrobní zakázky jako hotový deník. Pokud vaše organizace používá kategorie nákupu na nákupních objednávkách, můžete řídit požadavek na příjem povolením možnosti **Požadavky na příjem** pro pravidlo zásad kategorie na stránce **Zásady nákupu**.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Jak mohu zabránit uživateli, aby zaúčtoval dodací list prodejní objednávky, pokud ještě není zaúčtována výdejka prodejní objednávky?

Pokud ještě neproběhla výdejka prodejní objednávky, můžete uživateli zabránit v zaúčtování dodacího listu prodejní objednávky tím, že povolíte možnost **Požadavky na vyskladnění** pro skupinu modelů položek. Tato možnost se obvykle používá v organizacích, které provádějí fyzický proces vyskladnění ve skladu (například pomocí mobilního zařízení skladu k provádění vyskladnění). Možnost **Požadavek na vyskladnění** se vztahuje na *všechny* výdeje zásob pro položku, nejen pro prodejní objednávky. Například se vztahuje na deník zásob, který má záporné množství a deník výdejek výrobní zakázky.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Jak mohu zabránit uživateli, aby zaúčtoval fakturu prodejní objednávky, pokud ještě není zaúčtován dodací list prodejní objednávky?

Pokud ještě neproběhl dodací list prodejní objednávky, můžete uživateli zabránit v zaúčtování faktury prodejní objednávky tím, že povolíte možnost **Požadavky na srážku** pro skupinu modelů položek. Tato možnost se obvykle používá v organizacích, které provádějí fyzický proces balení ve skladu (například pomocí mobilní aplikace Warehouse Management k balení nebo generování dokumentu, který bude součástí dodávaných položek). Možnost **Požadavek na srážku** se vztahuje na *všechny* výdeje zásob pro položku, nejen pro prodejní objednávky. Například se vztahuje na deník zásob, který má záporné množství a deník výdejek výrobní zakázky.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Mohu zabránit prodeji registrovaných položek?

Když je položka registrována ve vašich zásobách v Supply Chain Management, množství je fyzicky k dispozici pro vydání v systému. Pokud položky, které byly zaregistrovány, ale dosud nebyly přijaty, by *neměly* být k dispozici pro vydání k prodejním objednávkám nebo výrobním zakázkám, zvažte například použití funkcí stavu zásob, blokování zásob, objednávek kvality, karanténních příkazů nebo rezervací pro řízení obchodního procesu.

## <a name="production-costing"></a>Výpočet nákladů výroby

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Mohu použít jeden nákladový model pro suroviny a jiný nákladový model pro hotové výrobky?

Ano, pro každou položku můžete použít různé nákladové modely. Není neobvyklé, že výrobci používají model periodických nákladů pro suroviny a standardní náklady pro polotovary a hotové výrobky.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Jak mohu snížit režijní náklady na stroje?

Chcete-li snížit režijní náklady na vaše stroje, musíte pro každý stroj vytvořit prostředky a skupiny prostředků podle vašich obchodních požadavků. Každý prostředek nebo skupinu prostředků lze přiřadit k cenovým kategoriím a řídit tak náklady na stroje. Každá nákladová kategorie může být propojena s nákladovou skupinou a každá nákladová skupina může být použita jako základ pro výpočet nepřímých nákladů v nákladovém formuláři.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Jak poznám náklady související se spotřebou energie (například spotřebou vody, energie nebo plynu) v nákladovém formuláři?

Náklady související se spotřebou energie můžete obecně uznat jedním ze dvou způsobů:

- Vytvořte řádek v kusovníku nebo receptuře. Obvykle je tento řádek vytvořen jako servisní položka a můžete zadat měrnou jednotku, kterou spotřebováváte, ve vztahu k množství, které vyrábíte. Tímto způsobem může uživatel během výrobního procesu spotřebovat různé množství. Položky můžete automaticky spotřebovat na základě hodnoty, kterou vyberete v poli **Princip odhlašování**.
- Vytvořte nepřímé náklady ve svém nákladovém formuláři. Obvykle se tento přístup používá k přidělení celkových nákladů na vaši spotřebu energie v rámci vašeho výrobního procesu. Nákladovou skupinu a absorpční základ můžete použít například ke škálování spotřeby na základě materiálů nebo práce na vaší trase.

Měli byste vybrat nejlepší možnost na základě vašich požadavků na hlášení, odsouhlasení a provoz.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Mohu zachytit podrobnosti o prostředku v kusovníku nebo receptuře?

Podrobnosti o zdroji lze zachytit pouze v operaci trasy. Ačkoli můžete vytvořit servisní položku, která má představovat prostředek, a přiřadit náklady ke zvýšení kalkulace nákladů na hotové zboží, tento přístup obvykle nedoporučujeme. Místo toho doporučujeme vytvořit jednoduchou trasu, která má jeden řádek pro sledování nákladů na prostředky, a nakonfigurovat operaci tak, aby byla automaticky spotřebována buď na začátku, nebo na konci výrobní zakázky.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Mohu zobrazit podrobnosti výpočtu, pokud jsou náklady zadány ručně?

Číslo Pokud ručně zadáte cenu na stránce **Cena položky**, tlačítka **Zobrazit podrobnosti výpočtu** a **Vykázat podrobnosti výpočtu** nejsou k dispozici. Pokud vyberete tlačítko **Shrnutí nákladů podle skupiny nákladů** pro nákladovou cenu, která se zadává ručně, zobrazí se souhrnný řádek a všechny náklady jsou zahrnuty k hotové položce zboží.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Vypočítá systém odchylky ve výrobní zakázce, když ručně zadávám náklady?

Ano, systém vypočítá odchylky, když ručně zadáte standardní náklady. Když však standardní náklady zadáte ručně místo jejich kalkulace, všechny spotřeby materiálu, trasy a nepřímých nákladů ve výrobní zakázce se považují za odchylku náhrazení. Pokud se vyskytnou další odchylky, jako je spotřeba materiálu nebo práce navíc, budou také zaznamenány jako odchylky z výrobního kusovníku. Proto důrazně doporučujeme, abyste vždy spustili kalkulaci pro položky, které mají kusovník, trasu nebo nepřímé náklady.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Jak mohu přenést odchylky z podřízené výrobní zakázky do nadřazené výrobní zakázky?

Když použijete model periodických nákladů, jako je FIFO, LIFO nebo vážený průměr, budou náklady z dílčí výroby uznány v heuristickém modelu, který jste pro položky vybrali. Pokud požadujete skutečné náklady, zvažte použití principu značení k označení, která dílčí výroba je vydána pro nadřazenou výrobní zakázku. Případně zvažte použití možnosti **Finanční zásoby** pro dimenzi **Dávka** nebo **Sériové číslo**, například ve skupině sledovacích dimenzí.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Jak princip vyprazdňování ovlivňuje spotřebu?

Princip vyprazdňování v kusovníku, receptuře nebo řádku trasy řídí načasování a techniku, která se používá ke spotřebě položky nebo práce. Pokud vyberete *Start*, položka nebo práce jsou automaticky spotřebovány při spuštění výrobní zakázky. Pokud vyberete *Konec*, položka nebo práce jsou automaticky spotřebovány při vykázání výrobní zakázky jako dokončené. Pokud vyberete *Ručně*, musí uživatel ručně vybírat materiály nebo zaznamenávat čas do deníku úlohy nebo karty trasy. Kusovníky a receptury mají také možnost *K dispozici na skladě*. Pokud vyberete tuto možnost, položky se automaticky spotřebují poté, co jsou přeneseny do umístění ve výrobním procesu.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Jak mám spustit kalkulace nákladů, pokud mám víceúrovňové kusovníky nebo receptury?

Obecně doporučujeme, abyste pro výpočet začínali na nejnižší úrovni vašich kusovníků nebo receptur. Chcete-li usnadnit filtrování při hromadných výpočtech nákladů, můžete použít skupiny výpočtů, které pomohou oddělit produkty. Doporučujeme také spustit pravidelnou úlohu *Přepočítat úrovně kusovníku*, než začnete hromadně počítat náklady. Každá organizace by měla zvážit kombinaci produktů a definovat strategii, která splňuje specifické potřeby vašeho produktu a struktury kusovníku nebo receptury.

## <a name="transfer-order-costing"></a>Výpočet nákladů převodního příkazu

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Existuje způsob, jak přiřadit dopravu k nákladům převodního příkazu?

K převodnímu příkazu můžete přidat poplatky a přidat tak náklady. Kód poplatků definuje debet a kredit pro poplatek, který přidáváte. Nejprve musíte vytvořit kódy poplatků v modulu **Řízení zásob**. Chcete-li k převodnímu příkazu přidat poplatek, vyberte **Poplatky** na řádku převodního příkazu, ke kterému chcete přidat poplatek.

## <a name="variances"></a>Odchylky

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Mohu s odchylkami zacházet jinak na základě pracoviště nebo skladu?

Neexistuje žádná možnost konfigurace účtů odchylek podle pracoviště. Když používáte standardní výpočet nákladů pro uvolněný produkt, můžete vybrat hlavní účet, který se používá pro účtování odchylek standardních nákladů na stránce **Účtování**. Můžete zvolit konfiguraci účtů pro jednu položku, skupinu položek nebo všechny položky. Můžete také nakonfigurovat jednu nákladovou skupinu, skupinu nákladových skupin nebo všechny nákladové skupiny.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Mohu oddělit odchylky, které jsou výsledkem směnných kurzů, od jiných typů odchylek?

Pokud je odchylka výsledkem rozdílu směnného kurzu mezi cenou nákupní objednávky a standardními náklady na položku, neexistuje způsob, jak oddělit směnný kurz od ostatních odchylek.

## <a name="reporting"></a>Vykazování

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Kolik konfigurací sestav hodnoty zásob mohu vytvořit a použít?

Počet konfigurací sestavy hodnot zásob, které můžete vytvořit, není omezen. Měli byste vyhodnotit své specifické požadavky na vytváření sestav a vytvořit počet konfigurací, které potřebujete ke splnění těchto požadavků. Ke spuštění sestavy nebo možnosti uložení sestavy budete potřebovat alespoň jednu konfiguraci sestavy hodnoty zásob.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Mohu použít sestavu hodnoty zásob k analýze nákladů na položku v každém skladu?

Ano. Můžete povolit možnost **Zobrazit** nebo **Celkový** pro každou dimenzi **Sklad** v konfiguraci sestavy hodnoty zásob. V sestavě se však zobrazí pouze hodnoty pro dimenze, které mají povolenou možnost **Finanční zásoby** pro skupinu dimenzí skladu. Pro ostatní dimenze zobrazí prázdné sloupce. Další informace viz [Příklady a logika sestavy hodnot zásob](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Jak mohu zobrazit množství zásob k určitému datu s váženým průměrem?

Můžete použít sestavu **Prodlení zásob**, která obsahuje sloupec **Průměrné náklady na jednotku**, který zobrazuje hodnotu zásob k určitému datu. Další informace viz [Příklady a logika sestavy prodlení zásob](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Jak mohu zobrazit, které transakce příjmu jsou vypořádány proti transakci výdeje?

Vyrovnání pro transakci zásob můžete zobrazit výběrem **Vyrovnání** nebo **Průzkumník nákladů** na kartě **Zásoby** v podokně akcí na stránce **Transakce zásob** nebo **Podrobnosti transakce zásob**. Pokud vyberete příjem pro zobrazení výdajů souvisejících s transakcí, průzkumník nákladů nezobrazí podrobnosti. Podrobnosti se zobrazí pouze v případě, že vyberete transakci výdeje.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Jak výkaz hodnoty zásob zobrazuje položky, které mají kladné fyzické množství a zápornou finanční hodnotu?

Výkaz hodnoty zásob odděluje fyzické a finanční částky a množství do vlastních sloupců. Hodnoty zobrazené v sestavě platí pro rozsah dat, který jste vybrali při spuštění sestavy. Zobrazená úroveň souhrnu závisí na nastavení, které jste vybrali. Pokud má položka transakce, které byly fyzicky přijaty a finančně vydány, množství a hodnoty se sečtou nezávisle. Pokud jste zvolili zobrazení úrovně podrobností jako transakce, řádky pro každý příjem a výdej se zobrazí samostatně a zobrazí se fyzické a finanční množství a částky. Další informace viz [Příklady a logika sestavy hodnot zásob](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Jaký je dopad skupin dimenzí úložiště a sledování na přehled hodnoty zásob?

Pokud povolíte možnost **Finanční hodnota** pro dimenzi ve skupině dimenzí úložiště nebo sledování, můžete vybrat možnost **Zobrazit** nebo **Celkem** pro dimenzi v konfiguraci sestavy hodnoty zásob. Pokud vyberete možnost **Zobrazit** nebo **Celkem** pro dimenzi, kde možnost **Finanční hodnota** není vybrána, bude sloupec ve výstupu sestavy prázdný. Pokud jste povolili možnost **Finanční hodnota** pro dimenzi ve skupině dimenzí úložiště nebo sledování a nevyberete možnost **Zobrazit** nebo **Celkem** v konfiguraci sestavy hodnot zásob, systém shrne hodnoty pro vybrané dimenze, kde jsou finančně sledovány.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Mohu přizpůsobit sestavy Power BI Embedded pro výpočet nákladů?

Ano, uživatelé, kteří mají správná bezpečnostní oprávnění, mohou aktualizovat plátno návrhu sestavy pro libovolnou sestavu Power BI Embedded v Supply Chain Management. Další informace viz [Přizpůsobit integrované sestavy v analytických pracovních prostorech](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Kde mohu zobrazit výkaz o analýze odchylek?

K výkazu o analýze odchylek se dostanete tak, že přejdete na **Cost management \> Dotazy a sestavy \> Účetnictví zásob – analytické sestavy** nebo **Cost management \> Dotazy a sestavy \> Účetnictví pro výrobu – analytické sestavy**. Obě možnosti otevřou stejnou sestavu a sestava má stejné chování.

## <a name="item-prices-and-default-costs"></a>Ceny položek a výchozí náklady

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Mohu spravovat náklady na každou variantu produktu?

Ano. Můžete povolit možnost **Použijte nákladovou cenu podle varianty** na pevné záložce **Správa nákladů** na stránce **Uvolněný produkt**, abyste umožnili stanovení cen podle varianty produktu. (Tato možnost je dostupná pouze pro základní produkty.) Poté na stránce **Cena položky** (kterou můžete otevřít buď ze stránky **Nákladová verze** nebo **Uvolněný produkt**) můžete vybrat **Zobrazení dimenzí** a určit, zda chcete zobrazit dimenzi **Konfigurace**, **Velikost**, **Barva** nebo **Styl**. Chcete-li uložit nastavení a použít vybrané dimenze při každém otevření stránky, povolte možnost **Uložit nastavení** a poté vyberte **OK**. Dimenze můžete zadat pouze pro položky, u kterých jsou dimenze aktivní ve skupině dimenzí produktu.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Mohu spravovat náklady na každý sklad?

Ne, nemůžete spravovat cenu položek podle skladu. Můžete však spravovat obchodní smlouvy pro nákupní ceny nebo prodejní ceny podle skladu. Nejprve vyberte možnost **Pro nákupní ceny** nebo **Pro prodejní ceny** pro dimenzi na stránce **Skupina dimenzí úložiště**. Poté, když vytvoříte deník obchodních smluv a otevřete řádky pro dimenze, vyberte **Zásoby \> Zobrazit dimenze** a vyberte, která dimenze se má zobrazit v mřížce. Chcete-li uložit nastavení a použít vybrané dimenze při každém otevření stránky, povolte možnost **Uložit nastavení** a poté vyberte **OK**. Dimenze můžete zadat pouze pro položky, u kterých jsou dimenze aktivní ve skupině dimenzí produktu.

### <a name="what-are-price-charges"></a>Co jsou cenové náklady?

Cenové náklady poskytují způsob, jak přidat pevnou částku k jednotkové ceně ceny položky nebo obchodní smlouvy. Když zadáte částku do pole **Cenové náklady**, můžete také zadat hodnotu do pole **Množství nákladů**. Cenové náklady budou amortizovány pro množství nákladů, které zadáte. Povolte možnost **Vč. v jednotkové ceně**, pokud chcete zahrnout cenové náklady do jednotkové ceny položky. Tato možnost je vždy povolena pro standardní náklady.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Jak mám nakonfigurovat ceny pro položky, které jsou pořizovány ve více měnách?

Pokud zadáte výchozí cenu v poli **Nákupní cena** na stránce **Uvolněný produkt**, předpokládá se, že je v účetní měně hlavní knihy právnické osoby, ve které se nacházíte. Stejně tak, pokud zadáte nákupní cenu v nákladové verzi, kde je pole **Typ ceny** nastaveno na *Nákupní*, předpokládá se cena v účetní měně vaší právnické osoby. Když vytvoříte nákupní objednávku pro dodavatele, který má jinou měnu, systém automaticky převede měnu z částky účetní měny na měnu transakce pomocí směnného kurzu, který zadáte v poli **Typ směnného kurzu účetní měny** ve vaší účetní knize.

Když vytváříte deník obchodních smluv, můžete na každém řádku zadat měnu, ve které vyjadřujete cenu. Můžete vytvářet obchodní smlouvy pro více měn, konkrétní dodavatele a mnoho dalších kombinací faktorů. Pokud vytvoříte nákupní objednávku, kde existuje obchodní smlouva pro měnu, kterou jste vybrali, systém použije obchodní smlouvu, která má odpovídající měnu. Když zaúčtujete transakce, jako jsou příjmy produktů nebo faktury, částka se převede na účetní měnu hlavní knihy pomocí směnného kurzu účetní měny, který zadáte v hlavní knize.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Jak mám nakonfigurovat náklady pro položky, které jsou pořizovány ve více měnách?

Náklady nelze konfigurovat ve více než jedné měně. Cena, kterou zadáte pro cenu položky nebo výchozí náklady, které zadáte do pole **Cena** pole na pevné záložce **Správa nákladů** ze stránky **Uvolněný produkt**, jsou vždy vyjádřeny v účetní měně hlavní knihy pro právnickou osobu, kterou jste vybrali.

Pokud vaše organizace používá standardní výpočet nákladů, měli byste definovat strategii pro definování nákladů, když existuje více měn. Měli byste také definovat proces pravidelné aktualizace nákladů, abyste snížili počet zaúčtovaných odchylek.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Mohu použít nastavení Zisk na stránce Nákladová skupina k výpočtu prodejních cen?

Ano, můžete použít nastavení **Zisk** na stránce **Nákladová skupina** a přidat procento při výpočtu prodejních cen pomocí kalkulace nákladů. Další informace naleznete v tématu [Výpočty kusovníku](bom-calculations.md).

## <a name="marking"></a>Označování

### <a name="how-does-marking-affect-periodic-costing-models"></a>Jak značení ovlivňuje modely periodických výpočtů nákladů?

Pokud používáte model periodických výpočtů nákladů, jako je FIFO, LIFO nebo vážený průměr, a označili jste transakci příjmu oproti transakci výdeje, bude heuristický model položky během procesu uzávěrky zásob ignorován. Namísto toho systém použije skutečné náklady příjmu pro náklady na výdej.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Co se stane během uzávěrky zásob, když použiji označení?

Když označíte příjemy a výdeje, uzávěrka zásob vypořádá transakce, které jsou označeny společně. Když se k vytvoření vyrovnání použije označení, pole **Zásady** na stránce **Vyrovnání** bude nastaveno na *Označení*. Pokud je transakce označena dříve, než je fyzicky nebo finančně aktualizována, problém použije náklady označeného příjmu namísto průběžných průměrných nákladů. Pokud jsou transakce označeny po finanční aktualizaci, proces uzávěrky a úpravy zásob upraví náklady na výdej, aby se odpovídaly nákladům na příjem.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Mohu ručně označit transakce, když používám standardní výpočet nákladů nebo klouzavý průměr?

Ne, nemůžete ručně označit příjmy nebo výdaje, když používáte standardní výpočet nákladů nebo klouzavý průměr. Pokud jsou transakce (například přímé dodávky nebo mezipodnikové objednávky) automaticky označeny, záznam o označení zůstane a bude fungovat jako pevná rezervace. Když však použijete standardní výpočet nákladů nebo klouzavý průměr, nemá označení záznamů žádný vliv na cenu položek.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Jak značení ovlivňuje výkaz zisků a ztrát?

Když označíte transakci výdeje oproti příjmu, náklady na výdej budou odpovídat vybranému příjmu. Když fyzicky a finančně záúčtujete výdej, zaúčtování ovlivní účty **Náklady prodaného zboží, dodané** a **Náklady prodaného zboží, fakturované**, které zadáte v profilu účtování zásob. Pokud je transakce označena po fyzické nebo finanční aktualizaci, proces *Uzávěrka a úprava zásob* vytvoří úpravu, která má odpovídající doklad, který upraví účet **Náklady prodaného zboží, fakturované** a protiúčet, který zadáte pro **Náklady jednotek, fakturované** (zásoby).

### <a name="how-does-marking-affect-master-planning"></a>Jak označení ovlivňuje hlavní plánování?

Karta **Standardní aktualizace** na stránce **Parametry hlavního plánování** obsahuje pole s názvem **Aktualizovat označení**. Volba, kterou tam vyberete, se použije při zakládání plánované zakázky, která je vygenerována hlavním plánováním. Existují tyto možnosti:

- *Ne* – Systém neprovádí žádné označení.
- *Standardní* – Systém označuje příjmy proti výdejům podle doložení. Objednávka požadavku se označí podle objednávky plnění. Pokud zbývá množství v plnění, objednávka plnění není označena.
- *Rozšířený* – Systém označí objednávky požadavku i objednávky plnění bez ohledu na to, zda v objednávce plnění zůstane otevřené nějaké množství nebo ne.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Záporné zásoby

### <a name="when-should-i-allow-physical-negative-inventory"></a>Kdy mám povolit záporné fyzické zásoby?

Obecně vám nedoporučujeme povolovat záporné fyzické zásoby, protože ve vašem skladu není možné mít méně než 0 (nulu) hmotné položky. Obchodní procesy některých odvětví a obchodních scénářů však mohou omezovat operace, které vyžadují, aby byly zásoby fyzicky záporné. Maloobchodníci například nemusí chtít zabránit prodeji položky, která je přinesena do registru, i když systém hlásí, že žádné položky nejsou k dispozici. Výrobci procesů poskytují další příklad. U těchto výrobců může spotřebované množství překročit to, co je doporučeno v receptuře. Alternativně může být spotřeba spíš odhadována než přesná, takže spotřeba překročí množství v určitém místě, jako je nádrž.

Kdykoli je to možné, měli byste zhodnotit svůj obchodní proces a pokusit se jej zlepšit, abyste zajistili, že zásoby nemohou být záporné. Pokud musíte povolit záporné zásoby, měli byste mít jasný obchodní proces pro opravu záporných zásob, protože to může nepříznivě ovlivnit výpočet nákladů.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Kdy mám povolit záporné finanční zásoby?

Obecně doporučujeme, aby většina organizací povolila záporné finanční zásoby. (Ve většině případů nejsou faktury nákupních objednávek zpracovány před odesláním položek.) Tuto možnost byste měli povolit, pokud máte specifické obchodní procesy, které vyžadují, aby prodejní cena odrážela konečné náklady nákupní objednávky. Tento požadavek může platit například v odvětví výroby na zakázku nebo ve specifických regionech, kde je to předepsáno zákonem.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Co se stane s náklady na mé výdeje, když jsou zásoby záporné?

Když jsou zásoby pro vaši položku záporné a vydáte více položek, než fyzicky máte, systém použije výchozí cenu položky k výpočtu průběžného průměru, pokud používáte model periodického výpočtu nákladů, jako je FIFO, LIFO nebo vážený průměr. Pokud není u položky zadána výchozí cena, systém vydá zásoby s hodnotou 0 (nula). Toto chování může způsobit, že budoucí výpočty vašeho průběžného průměru nebo klouzavého průměru budou nepřesné.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Mohu zabránit tomu, aby byly položky vyskladněny, baleny nebo prodávány na základě prodejních a výrobních zakázek, pokud není dostatek zásob na skladě?

Ano. Doporučujeme zakázat možnost **Záporné fyzické** pro skupinu modelů položek, a zabránit tomu, aby byly položky vyskladňovány, baleny nebo prodávány na základě prodejních a výrobních zakázek.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Mohu zabránit fakturaci položek na prodejní objednávce, pokud nebyly pro stejnou položku fakturovány žádné nákupní objednávky?

Ano. Doporučujeme zakázat možnost **Záporné finanční** pro skupinu modelů položek, a zabránit tak fakturaci položek na prodejní zakázce, pokud nebyly pro stejnou položku fakturovány žádné nákupní objednávky.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Jak záporné zásoby ovlivňují finanční poměry, jako je hrubá zisková marže?

Když povolíte, aby se vaše zásoby dostaly do záporných hodnot, hodnota zásob ve vaší rozvaze a náklady na prodané zboží ve výkazu zisků a ztrát mohou být podhodnoceny, zvláště pokud pro vaše položky není nakonfigurována žádná výchozí cena. Proto mohou být finanční výkazy a poměry, jako jsou hrubé ziskové marže, nadhodnoceny, protože náklady jsou nesprávné. Pokud používáte model periodických výpočtů nákladů, jako je FIFO, LIFO nebo vážený průměr, hodnotu výdejů lze upravit, když spustíte proces uzávěrky a úpravy zásob poté, co byla opravena záporná množství zásob. Pokud však použijete klouzavý průměr, neexistuje způsob, jak jednotlivé transakce přecenit.

### <a name="how-should-i-correct-negative-inventory"></a>Jak mám opravit záporné zásoby?

Doporučujeme, abyste často monitorovali a opravovali záporné zásoby, pokud vaše organizace nebo obchodní požadavky vyžadují, abyste povolili záporné zásoby. Hodnoty zásob můžete opravit provedením počítání cyklů, zaúčtováním úpravy nebo zaúčtováním deníku pohybů. Pokud musíte uznat neočekávané nárůsty zásob na konkrétním účtu hlavní knihy, měli byste naplánovat použití deníku pohybů. V opačném případě, když použijete počítání cyklů nebo proces úpravy zásob, systém zaúčtuje úpravu zásob na účet **Příjem zásob** a protiúčet **Výdaje zásob, zisk**, které zadáte v profilu účtování zásob.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Musím vytvořit novou položku, pokud se moje zásoby dostaly do záporné hodnoty a používám klouzavý průměr?

Číslo Pokud vaše organizace umožňuje, aby zásoby byly fyzicky záporné a jako model zásob používáte klouzavý průměr, systém použije posloupnost záložních nákladů, která je přiřazena na stránce **Parametry modulu Řízení zásob a skladu** a určí, jak budou náklady přiřazeny k vašim výdejům. Obecně doporučujeme, abyste nepovolovali, aby se vaše zásoby dostaly do fyzického záporu. Více informací naleznete mezi dalšími otázkami v sekci [Záporné zásoby](#negative-inventory) v tomto článku.

## <a name="not-stocked-products"></a>Produkty, které nejsou na skladě

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Mohu zaúčtovat výdejky prodejních objednávek pro produkty, které nejsou na skladě?

Když generujete výdejku pro prodejní objednávku, která obsahuje položky, které jsou ve skupině modelu položek, která není na skladě, neuvidíte žádné řádky pro tyto položky, které nejsou na skladě. Ke zpracování položek, které nejsou na skladě, nelze použít mobilní aplikaci Warehouse Management

Když generujete dodací list pro prodejní objednávku, která obsahuje položky, které jsou ve skupině modelů položek, která není na skladě, nastavte pole **Množství** ns *Vybráno množství a neskladované produkty* k zahrnutí nenaskladněných položek do generování dokladu. Pokud vyberete *Vše*, do dodacího listu budou zahrnuty pouze skladové položky.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Mám použít produkt, který není na skladě, nebo kategorii (kategorie prodeje nebo kategorie zásobování)?

Volba mezi produktem, který není skladem, a kategorií závisí na vašich konkrétních obchodních požadavcích. Produkty, které nejsou na skladě, obecně nabízejí větší kontrolu nad výchozími hodnotami, jako jsou množství a ceny v nákupních objednávkách a prodejních objednávkách. Proto jsou preferovány produkty, které nejsou na skladě, ve scénářích, kdy je stejný produkt nebo služba zakoupena nebo prodána více než jednou. Kategorie jsou užitečné ve scénářích, kde jsou cena, položky, popisy atd. u jednotlivých transakcí nekonzistentní. Kategorie lze také použít na jakýkoli produkt, aby pomohly klasifikovat typ produktu, který se prodává nebo kupuje.

## <a name="service-items"></a>Servisní položky

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Jaký je rozdíl mezi servisní položkou a produktem, který není na skladě?

Servisní položka je typem produktu. Když vytváříte nově uvolněný produkt, můžete nastavit pole **Typ produktu** buď na *Položku* nebo *Servis*. *Položka* je obvykle vybrána k označení, že položka je hmotná, zatímco *Servis* je obvykle vybrán k označení, že položka je nehmotná.

Jakýkoli uvolněný produkt, bez ohledu na to, zda se jedná o položku nebo produkt služby, může být na skladě nebo ne. Nastavení na skladě nebo ne se řídí skupinou modelů položek, kterou vyberete pro uvolněný produkt. Když vyberete skupinu položek, která není na skladě, systém nevytvoří například transakce zásob pro související prodejní objednávku nebo nákupní objednávku.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Mohu do kusovníku zahrnout položky, které nejsou skladem?

Ne, nemůžete zahrnout uvolněný produkt, který je propojen se skupinou modelů položek, kde je možnost **Na skladě** v kusovníku nebo receptuře zakázána. Nezáleží na tom, zda je pole **Typ produktu** nastaveno na *Položku* nebo *Servis*. Do řádků kusovníku nebo receptur lze zahrnout pouze položky, které jsou na skladě.

## <a name="costing-modelspecific-questions"></a>Otázky specifické pro model výpočtu nákladů

### <a name="which-costing-model-should-i-use"></a>Jaký model výpočtu nákladů bych měl použít?

Modely výpočtu nákladů, které byste měli vybrat, závisí na požadavcích vaší firmy. Než vyberete model výpočtu nákladů pro použití v Supply Chain Management, měli byste ověřit, že je model povolen podle místních předpisů. Doporučujeme, abyste si svůj výběr ověřili u certifikovaného účetního ve vašem regionu.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Mohu ve své organizaci používat více než jeden model výpočtu nákladů?

Ano. Počet skupin modelů položek nebo modelů výpočtu nákladů, které můžete vybrat v Supply Chain Management, není omezen.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Mohu pro každou položku používat více než jeden model výpočtu nákladů?

Číslo Pro každý uvolněný produkt můžete vybrat pouze jeden model výpočtu nákladů. Toto chování je řízeno skupinou modelů položek. Pokud musíte k vykazování hodnot zásob použít více než jeden model výpočtu nákladů, měli byste zvážit použití doplňku Globální účtování zásob.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Jakou metodu výpočtu nákladů bych měl použít, když používám provádění výroby?

Modely výpočtu nákladů, které byste měli vybrat, závisí na požadavcích vaší firmy. Neexistuje žádná konkrétní výhoda ani nevýhoda použití jakéhokoli modelu výpočtu nákladů, když vaše organizace také používá provádění výroby.

### <a name="when-is-fefo-used"></a>Kdy se používá FEFO?

Nejdříve končící platnost, nejdříve ze skladu (FEFO) není metodikou výpočtu nákladů. Místo toho se jedná rezervační techniku, která se často používá ve výrobních organizacích. Rezervace FEFO pro skupinu modelů položek můžete aktivovat povolením možnosti **Řízení FEFO podle data** a poté výběrem hodnoty v poli **Kritéria vyskladnění**.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Má výběr jednoho modelu výpočtu nákladů oproti jinému výhody z hlediska výkonu?

Obecně platí, že model výpočtu nákladů, který vyberete pro položku, má minimální dopad na celkový výkon systému. Doba potřebná ke spuštění procesu uzávěrky nebo přepočtu zásob však může být ovlivněna modelem výpočtu nákladů na zásoby, který vyberete. Pokud například používáte standardní náklady nebo klouzavý průměr, proces uzavírky zásob má minimální dopad na systém, protože neaktualizuje každou transakci zásob a nevytváří vyrovnání. Model periodických výpočtů nákladů, jako je FIFO, LIFO nebo vážený průměr, však může prodloužit dobu potřebnou k dokončení procesu uzávěrky zásob. Konkrétně může být proces uzávěrky delší, když zadáte vysoké číslo do pole **Maximální počet iterací povolený na zboží** nebo nízké číslo do pole **Minimální povolená částka** pro proces *Uzávěrka zásob*.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Kdy mám použít možnost Pevná cena příjmu?

Když vyberete zaškrtávací políčko **Pevná cena příjmu** na stránce **Skupina modelů položek** pro položku, systém použije cenu příjmu jako standardní cenu pro příjem zásob. Pokud je rozdíl mezi nákupní cenou a výchozí nákladovou cenou položky, která je nakonfigurována pro produkt, rozdíl se zaúčtuje na účet **Pevná cena příjmu - zisk** nebo **Pevná cena příjmu - ztráta** a na protiúčet **Fixní cena příjmu - protiúčet**. (Všechny tyto účty jsou uvedeny na stránce **Účtování**.)

Měli byste vybrat zaškrtávací políčko **Pevná cena příjmu**, když používáte model periodických výpočtů nákladů, jako je FIFO, LIFO nebo vážený průměr, a požadujete, aby byl v hlavní knize sledována odchylka nákupní ceny, pokud se cena příjmu liší od výchozí ceny položky.

### <a name="moving-average"></a>Klouzavý průměr

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Je klouzavý průměr stejný jako plovoucí průměr?

Termíny klouzavý průměr, plovoucí průměr a průběžný průměr se často používají jako synonyma. Z těchto pojmů je klouzavý průměr jediným oficiálním modelem výpočtu nákladů, který je dostupný v Supply Chain Management. Přestože průběžný průměr není oficiální model výpočtu nákladů, je to technika, která se používá, když používáte model periodických výpočtů nákladů, jako je FIFO, LIFO nebo vážený průměr. Termín plovoucí průměr se v Supply Chain Management nepoužívá a v jiných systémech může mít různé konotace.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Jak mohu přizpůsobit rozdíl mezi cenou příjmu produktu a cenou na faktuře, když použiji klouzavý průměr?

Když použijete klouzavý průměr, fyzické náklady (cena příjmu) se použijí k výpočtu klouzavého průměru pro všechny transakce výdeje. Pokud existuje rozdíl mezi fyzickými náklady (cena na příjmu) a finančními náklady (cena na faktuře), systém automaticky zaúčtuje rozdíl na hlavní účet, který je zadaný pro typ účtování **Cenový rozdíl pro klouzavý průměr** na kartě **Zásoby** na stránce **Profil účtování zásob**.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Kde je cenový rozdíl pro klouzavý průměr uvedený v hlavní knize?

Pokud existuje cenový rozdíl mezi zaúčtováním fyzické aktualizace a finanční aktualizace pro příjem, rozdíl se zaúčtuje na hlavní účet, který je zadaný pro typ účtování **Cenový rozdíl pro klouzavý průměr** na kartě **Zásoby** na stránce **Profil účtování zásob**. Další informace viz [Klouzavý průměr](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Když použiji klouzavý průměr, co se stane, když dojde k výdeji před příjmem?

Obvykle se může vyskytnout výdej před příjmem buď proto, že povolujete fyzické záporné zásoby pro skupinu modelů položek, nebo proto, že je výdej datován zpětně. Více informací najdete v části [Záporné zásoby](#negative-inventory) v tomto článku.

Pokud provádíte zpětné datování transakcí, doporučujeme vám pečlivě zvážit svůj obchodní proces a operace, abyste zjistili, zda existuje způsob, jak se tomuto scénáři vyhnout. Pokud provedete zpětné datování transakce pro položku, která používá klouzavý průměr, systém transakci přiřadí aktuální klouzavý průměr. Pozdější výdeje nejsou upraveny. Další informace o klouzavém průměru se zpětně datovanými transakcemi naleznete v části [Klouzavý průměr](moving-average.md).

### <a name="standard-costing"></a>Standardní výpočet nákladů

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Jaký je rozdíl mezi standardním výpočtem nákladů a pevnou cenou příjmu?

Standardní výpočet nákladů vyžaduje, abyste definovali cenu položky a aktivovali náklady ve verzi výpočtu nákladů. Tyto náklady se používají pro všechny příjmy a výdeje. Odchylky pro příjmy do zásob se zaznamenávají do hlavní knihy pomocí standardních účtů odchylek nákladů, které zadáte na kartě **Standardní náklady** stránky **Profil účtování zásob**.

Když však použijete pevnou cenu příjmu, budou pevné pouze náklady na příjmy a systém použije náklady, které zadáte na pevné záložce **Správa nákladů** na stránce **Uvolněný produkt**. Rozdíly mezi výchozími náklady a cenou nákupní objednávky způsobí, že odchylka nákupní ceny bude zaúčtována na účty zisků a ztrát s pevnou cenou příjmu. Výdeje nepoužívají pevnou cenu příjmu. Místo toho budou výdeje oceněny průběžným průměrem v době zaúčtování (pokud nepoužijete označení) a budou přeceněny dle heuristického modelu, který vyberete při spuštění uzávěrky zásob.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Mohu použít rezervace FEFO se standardním výpočtem nákladů?

Ano, můžete použít rezervace FEFO v modelové skupině položek, když vyberete standardní výpočet nákladů. Rezervace FEFO řídí rezervační logiku, která se používá pro fyzickou manipulaci s položkami, zatímco standardní výpočet nákladů řídí fyzické a finanční náklady na položku.

### <a name="can-i-upload-pending-prices"></a>Mohu odeslat nezpracované ceny?

Ano, k nezpracované ceny můžete použít doplněk Excel nebo rozhraní Data Management Framework. Doporučujeme používat následující entity:

- Nezpracované ceny položek (V2)
- Čekající jednotkové náklady kategorie nákladů postupu
- Faktory výpočtu uzlu nákladového formuláře (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Jak často mohu aktualizovat standardní náklady položky?

Frekvence, ve které můžete aktivovat nové standardní náklady, není nijak omezena. Pokud aktivujete nové náklady pro položku ve stejný den, kdy byly aktivovány poslední náklady, systém použije u nových transakcí nebo aktualizací (jako jsou aktualizace stávajících transakcí) poslední aktivované náklady.

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Mohu deaktivovat nebo odstranit aktivované náklady?

Ne, deaktivovat nebo odstranit aktivované náklady není možné. Pokud jste nesprávně aktivovali náklady, můžete aktivovat nové náklady, které jsou správné.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Používají se kalkulační skupiny se standardním výpočtu nákladů?

Kalkulační skupiny lze použít s jakoukoli položkou bez ohledu na vybranou skupinu modelů položek. Kalkulační skupiny se používají během procesu kumulace nákladů nebo výpočtu nákladů k určení nastavení, která by se měla použít pro položky, pro které spouštíte výpočet. Další informace o kalkulačních skupinách naleznete v tématu [Kalkulační skupiny kusovníků](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Kdy bych měl použít plánovanou verzi výpočtu nákladů?

Verze výpočtu nákladů mohou mít typ *Standardní náklady* nebo *Plánované náklady*. Typ *Standardní náklady* se používá pro náklady, které jsou aktivní v systému a budou zaúčtovány v transakcích. Typ *Plánované náklady* se používá pro provádění simulací nákladů a neovlivňuje náklady na transakce.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Lze celkové náklady z jedné entity převést na jinou entitu jako prodejní náklady?

Neexistuje žádný automatický způsob, jak kopírovat náklady z jedné společnosti do druhé. Navíc neexistuje žádný automatický způsob, jak zkopírovat náklady z nákupní ceny do prodejní ceny. Pokud vaše organizace musí dokončit jeden z těchto úkolů, zvažte, zda můžete použít rozhraní Data Management Framework k exportu dat z vaší verze výpočtu nákladů a odeslání do jiné společnosti, buď jako prodejní cenu ve verzi výpočtu nákladů nebo jako obchodní smlouvu. Může být vyžadována ruční manipulace se soubory.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Jaký je nejlepší způsob kopírování plánovaných nákladů do standardního výpočtu nákladů?

Můžete použít tlačítko **Kopírovat** na stránce **Verze výpočtu nákladů** pro kopírování cen položek, cen kategorií nákladů nebo nepřímých nákladů z jedné verze výpočtu nákladů do jiné.
