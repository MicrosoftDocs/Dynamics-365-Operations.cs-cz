---
title: Odložené transakce ve fakturaci předplatného
description: Toto téma popisuje různé transakce, které lze použít v odložených transakcích jako součást odložení výnosů a nákladů ve fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f66c538afc732caf3faed3cfea6c695ff7f16273
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/08/2022
ms.locfileid: "8558091"
---
# <a name="deferral-default-transactions"></a>Odložené výchozí transakce

Toto téma popisuje transakce, které umožňují odkládání výnosů a výdajů. Harmonogramy odkladů jsou vždy založeny na původním dokumentu nebo rozvrhu fakturace a závisí na nich. Plány odkladů jsou vytvářeny na základě výchozích hodnot a nelze je zadávat ani vytvářet samostatně.

## <a name="sales-order-transaction-deferral"></a>Odložení transakce prodejní objednávky

Použijte stránku **Odklady** nebo **Vytvořte dobropis** pro zadání nebo úpravu parametrů odložení pro řádek prodejní objednávky.

> [!NOTE]
> Když je prodejní objednávka vytvořena z plánu fakturace, všechny hodnoty na stránce **Odklady** nebo **Vytvořte dobropis** jsou pouze pro čtení a parametry odložení nelze upravovat. Chcete-li upravit hodnoty, použijte stránku **Upravit plán**.

### <a name="edit-deferral-options"></a>Upravit možnosti odkladu

Chcete-li upravit možnosti odložení pro řádek, postupujte takto.

1. Vytvořte transakci prodejní objednávky.
2. Vyberte řádek a poté vyberte **Odklady**.
3. Na stránce **Odložení transakce** musí být možnost **Odložený** nastavena na **Ano**. V případě potřeby upravte další pole.
4. Chcete-li zobrazit náhled plánu odkladu, vyberte volbu **Náhled**.
5. Pokud jste provedli nějaké změny v odložení transakce, vyberte **OK** a vraťte se na stránku transakce.
6. Potvrďte a odešlete transakci.

Po zaúčtování transakce otevřete stránku **Všechny plány odkladů** pro zobrazení plánu odkladu.

### <a name="create-a-credit-note"></a>Vytvoření dobropisu

Dobropis vytvoříte takto.

1. Vytvořte transakci prodejní objednávky.
2. V sekci **Řádky prodejní objednávky** vyberte položku, pro kterou chcete vytvořit dobropis.
3. Vyberte **Řádek prodejní objednávky** \> **Nový** a poté vyberte **Dobropis**.
4. Vyberte **Odklady**.
5. Na stránce **Odložení transakce prodejní objednávky** nastavte možnost **Upravit stávající plán** na **Ano** pro položku.
6. V poli **Upravený plán** vyberte plán odkladu, na který chcete dobropis použít.
7. Aktualizujte pole **Přepočítat datum** a **Datum ukončení**, jak požadujete.
8. Vyberte **OK**.
9. Dokončete zaúčtování transakce prodejní objednávky.

### <a name="purchase-orders-and-purchase-invoices"></a>Nákupní objednávky a nákupní faktury

Pokud chcete použít funkci odkladu pro nákupní objednávku, vygenerujte nejprve fakturu. Poté použijte stránku **Nevyřízené faktury dodavatele**, chcete-li upravit nebo přidat odložené položky. Přímo v nákupní objednávce nemůžete upravit ani přidat odklady.

1. Použijte stránku **Nevyřízené faktury dodavatele** pro zadání faktury dodavatele.

    Když zadáte řádek, odklad se automaticky nastaví pro položku nebo kategorii nákupu, kterou vyberete. Tento odklad je založen na nastavení odkladu na stránce **Výchozí hodnoty odkladu**. Odložení lze upravit nebo přidat na úrovni distribuce.

3. Na nákupním řádku vyberte **Finance \> Distribuce částek**.
4. Pro každou distribuční částku vyberte **Odklady**. Při zaúčtování faktury se vytvoří plán odkladu pro každou distribuci, pro kterou je odklad nastaven.

### <a name="tax"></a>Daň

V některých případech může být částka daně zcela nebo částečně nevratná. Pokud částka daně v odložitelném řádku obsahuje nevratnou částku, bude nevratná částka daně zahrnuta do částky odložitelného plánu při zaúčtování faktury.

### <a name="variance"></a>Odchylka

Pokud se částka na řádku faktury dodavatele liší od částky na řádku nákupní objednávky, vytvoří se rozdělení odchylek. Pokud je řádek odložen, účet hlavní knihy pro tyto distribuce je nastaven na účet odkladu a částky jsou zahrnuty do částky časového rozvrhu při zaúčtování faktury. Tyto distribuce jsou pojmenovány **Cenová odchylka** a **Odchylka nákladů**.

### <a name="general-journals-and-invoice-journals"></a>Hlavní deníky a deníky faktur

Použijte stránku **Odklady** pro zadání parametrů odložení pro řádek dokladu deníku. Můžete si také zobrazit náhled plánu odkladu pro odložení řádků. Když zadáte řádek, odklad se automaticky nastaví na základě nastavení účtů odkladu na stránce **Výchozí hodnoty odkladu**. Možnosti odkladu můžete ručně změnit pro každý řádek. Po zaúčtování dokladu deníku se vytvoří plán odkladu.

#### <a name="post-and-transfer"></a>Zaúčtovat a převést

K zaúčtování poukázky deníku použijte příkaz **Zaúčtování a převod**. Možnosti odkladu budou následovat po řádku, na který se voucher vztahuje. Pro poukázky, které neobsahují chyby, se vytvoří plán odložení, pokud je odložen. U voucheru, který má chybu a jsou převedeny, se s ním přenášejí i případné možnosti odkladu.

#### <a name="tax"></a>Daň

V některých případech může být částka daně zcela nebo částečně nevratná. Pokud částka daně v odložitelném řádku obsahuje nevratnou částku, bude nevratná částka daně zahrnuta do částky odložitelného plánu při zaúčtování faktury.

## <a name="free-text-invoice-transaction-deferral"></a>Odklad transakce volné faktury

Použijte stránku **Odklady** pro zadání parametrů odložení pro distribuci řádku volné faktury. Když je zadána distribuce, odklad se automaticky nastaví na základě nastavení odkladu na stránce **Výchozí hodnoty odkladu**.

## <a name="fields"></a>Pole

Stránka **Odklad transakce** obsahuje následující pole.

| Pole | Popis |
|-------|-------------|
| Odloženo | <p>Určete, zda je řádek odložený:</p><ul><li>**Ano** - Řádek je odložený.</li><li>**Ne** - Řádek není odložený.</li></ul><p>Když je tato možnost nastavena na **Ano**, možnost **Upravit stávající plán** není k dispozici. U položek a poplatků, které jsou již nastaveny jako odložené, je tato možnost nastavena na **Ano**. U položek a poplatků, které nejsou nastaveny jako odložené ve výchozím nastavení, nastavte tuto možnost na **Ano**.</p> |
| Upravit existující plán | <p>Zadejte, zda je řádek úpravou stávajícího plánu odkladu:</p><ul><li>**Ano** - Nový prodejní řádek je úpravou stávajícího plánu odkladu. V tomto případě si můžete vybrat plán odkladu v poli **Upravený plán**.</li><li>**Ne** - Nový prodejní řádek není úpravou stávajícího plánu odkladu.</li></ul><p>Když je tato možnost nastavena na **Ano**, možnost **Odloženo** není k dispozici.</p> |
| Upravený plán | <p>Vyberte plán odložení, který řádek upravuje. Všechny hodnoty na stránce jsou poté aktualizovány hodnotami z původního plánu odložení. Tyto hodnoty nelze upravit.</p><p>Toto pole je k dispozici pouze, pokud je možnost **Upravit stávající plán** nastavena na **Ano**.</p> |
| Datum přepočtu | <p>Zadejte datum začátku období, ze kterého chcete přepočítat zbývající částku. Výchozí datum je datum dalšího nerozpoznaného období.</p><p>Toto pole je k dispozici pouze, pokud je možnost **Upravit stávající plán** nastavena na **Ano**.</p> |
| Datum ukončení | <p>V závislosti na typu odkladu může nebo nemusí být datum ukončení aktualizováno:</p><ul><li>V případě přímého odložení určete nové datum ukončení plánu. Stávající datum ukončení plánu odkladu je výchozí hodnotou.</li><li>V případě odkladu na základě události zadejte datum ukončení hranice kreditní události. Toto datum může být prázdné.</li></ul><p>Toto pole je k dispozici pouze, pokud je možnost **Upravit stávající plán** nastavena na **Ano**.</p> |
| Číslo plánu fakturace | <p>Číslo plánu fakturace.</p><p>Toto pole je dostupné pouze pro opakující se plány fakturace smlouvy.</p> |
| Způsob úpravy odkladu | <p>Metoda odložené úpravy. Hodnota odpovídá hodnotě na stránce **Zpracování hromadného ukončení** pro opakující se plán fakturace smlouvy.</p><p>Toto pole je dostupné pouze pro opakující se plány fakturace smlouvy.</p> |
| **Účty - Výnosy** | |
| Účet pro odklad | <p>Odložený účet, což je účet pro zaúčtování, který se zobrazuje na stránce **Prodejní objednávka**.</p><p>Pokud řádek není odložen, je toto pole prázdné. V tomto případě je účtovací účet výchozím účtem výnosů.</p> |
| Účet pro uznání | <p>Zadejte účet, který se použije, když je rozpoznáno odložení. Tento účet se musí lišit od účtu odkladu.</p><p>Když je možnost **Odložený** zpočátku nastavena na **Ano**, hodnoty dimenzí, které se používají na účtu odkladu, se zkopírují na účet uznání. Pokud dimenze v účtu odložení pro účet uznání neexistuje, bude ignorována.</p> |
| Účet pro prvotní uznání | <p>Vyberte účet pro počáteční uznání výnosů. Výchozí hodnota je ze stránky **Výchozí hodnoty odkladu**.</p><p>Toto pole je dostupné pouze tehdy, když je pole **Metoda odloženého zaúčtování** nastaveno na **Zisk a ztráta** na stránce **Parametry odložení výnosů a nákladů**.</p> |
| Ofsetový účet uznání | <p>Vyberte protiúčet pro uznání výnosů. Výchozí hodnota je ze stránky **Výchozí hodnoty odkladu**.</p><p>Toto pole je dostupné pouze tehdy, když je pole **Metoda odloženého zaúčtování** nastaveno na **Zisk a ztráta** na stránce **Parametry odložení výnosů a nákladů**.</p> |
| **Účty - slevy** | Tato sekce se zobrazí pouze pro odložené položky. Je skryta pro odložené poplatky. |
| Účet pro odklad | <p>Zadejte číslo účtu pro odložení slevy. Výchozí hodnota je ze stránky **Výchozí hodnoty odkladu**.</p><p>Toto pole je dostupné pouze tehdy, když je pole **Možnost odkladu slevy** nastaveno na **Samostatný plán pro slevu** na stránce **Parametry odložení výnosů a nákladů** a na řádek se uplatní sleva.</p> |
| Účet pro uznání | <p>Zadejte číslo účtu pro uznání slevy. Výchozí hodnota je ze stránky **Výchozí hodnoty odkladu**.</p><p>Toto pole je dostupné pouze tehdy, když je pole **Možnost odkladu slevy** nastaveno na **Samostatný plán pro slevu** na stránce **Parametry odložení výnosů a nákladů** a na řádek se uplatní sleva.</p> |
| Účet pro prvotní uznání | <p>Vyberte účet pro počáteční uznání slevy. Výchozí hodnota je ze stránky **Výchozí hodnoty odkladu**.</p><p>Toto pole je dostupné pouze tehdy, když je pole **Metoda zaúčtování odkladu** nastaveno na **Zisk a ztráta** na stránce **Parametry odložení výnosů a nákladů** a na řádek se uplatní sleva.</p> |
| Ofsetový účet uznání | <p>Vyberte protiúčet pro uznání výnosů. Výchozí hodnota je ze stránky **Výchozí hodnoty odkladu**.</p><p>Toto pole je dostupné pouze tehdy, když je pole **Metoda zaúčtování odkladu** nastaveno na **Zisk a ztráta** na stránce **Parametry odložení výnosů a nákladů** a na řádek se uplatní sleva.</p> |
| **Účty - Spotřeba** | Tato sekce se zobrazí pouze pro odložené položky. Je skryta pro odložené poplatky. |
| Účet pro odklad | <p>Zadejte číslo účtu pro odložení spotřeby.</p><p>Pro standardní produkty jsou vytvořeny dva plány odkladů:</p><ul><li>**Standardní prodej** – Plán příjmů, který má kreditní zůstatek. V tomto případě vyberte účet odložení spotřeby.</li><li>**Spotřeba** – Plán výdajů na spotřebu (náklady na prodané zboží \[COGS\]), který má debetní zůstatek. V tomto případě vyberte účet uznání spotřeby.</li></ul><p>Při zaúčtování faktury se částka spotřeby zaúčtuje na zadaný účet odkladu spotřeby. Tato pole nejsou dostupná pro servisní položky.</p> |
| Účet pro uznání | Zadejte číslo účtu pro uznání spotřeby. |
| Účet pro prvotní uznání | <p>Zadejte účet pro počáteční vykazovanou částku spotřeby. Výchozí hodnota je ze stránky **Výchozí hodnoty odkladu**.</p><p>Toto pole je dostupné pouze tehdy, když je pole **Metoda odloženého zaúčtování** nastaveno na **Zisk a ztráta** na stránce **Parametry odložení výnosů a nákladů**.</p> |
| Ofsetový účet uznání | <p>Zadejte protiúčet pro vykazovanou částku spotřeby. Výchozí hodnota je ze stránky **Výchozí hodnoty odkladu**.</p><p>Toto pole je dostupné pouze tehdy, když je pole **Metoda odloženého zaúčtování** nastaveno na **Zisk a ztráta** na stránce **Parametry odložení výnosů a nákladů**.</p> |
| **Plán** | |
| Typ plánu | <p>Vyberte typ plánu odložení: **Lineární** (výchozí) nebo **Na základě události**.</p><p>Možnosti zobrazené na stránce jsou založeny na typu plánu odkladu, který vyberete.</p><p>Pokud je výchozí šablona nastavena na stránce **Výchozí hodnoty odkladu** pro řádek transakce, typ plánu odkladu je založen na typu vybrané šablony.</p> |
| **Plán - Lineární** | |
| Konsolidovat předchozí období | <p>Určete, zda chcete konsolidovat řádky plánu odkladu za dřívější období:</p><ul><li>**Ano** – Konsolidujte řádky plánu odkladu pro dřívější období.</li><li>**Ne** – Nekonsolidujte řádky plánu odkladu pro dřívější období.</li></ul><p>Výchozí hodnota je ze stránky **Parametry odkladu výnosů a nákladů**.</p> |
| Stejné za období | <p>Zadejte, zda je počet dní v každém období stejný nebo se liší podle období:</p><ul><li>**Ano** – Každé období má stejný počet dní.</li><li>**Ne** – Období nemají stejný počet dní.</li></ul><p>Když je tato možnost nastavena na **Ne**, počet dní v období se bere v úvahu při výpočtu částky v každém období pro plán odkladu.</p><p>Výchozí hodnota je ze stránky **Parametry odkladu výnosů a nákladů**.</p> |
| Plán ze šablony | <p>Zadejte, zda je plán odkladu vytvořen na základě šablony nebo data ukončení:</p><ul><li>**Ano** – Plán odkladu je vytvořen na základě šablony.</li><li>**Ne** - Plán odkladu je vytvořen na základě koncového data.</li></ul> |
| Šablona | Vyberte šablony odkladu. |
| Počáteční datum přepsání | <p>Určete, zda chcete přepsat počáteční datum:</p><ul><li>**Ano** – Přepište počáteční datum datem, které zadáte do pole **Počáteční datum**.</li><li>**Ne** – Počáteční datum je pravidlem **Výchozí datum zahájení odkladu**, které se použije na datum faktury uvedené na stráce **Zaúčtování faktury**. Toto pravidlo lze nastavit na stránce **Parametry odkladu výnosů a nákladů**.</li></ul> |
| Počáteční datum odkladu | Zadejte počáteční datum odkladu. Výchozí hodnotou je datum transakce. |
| Koncové datum odkladu | <p>Koncové datum odkladu.</p><p>Toto datum se automaticky vypočítá na základě šablony odkladu. Pokud není vybrána žádná šablona, musíte datum zadat ručně.</p> |
| **Plán – na základě události** | |
| Šablona | <p>Vyberte šablonu založenou na události. Toto pole je volitelné.</p><p>Pokud vyberete šablonu, hodnoty ze šablony přepíší všechna data a řádky událostí založené na událostech.</p> |
| Typ přidělení | <p>Vyberte typ přidělení pro řádky událostí:</p><ul><li>**Variabilní částky** – konkrétní částka přidělení je vložena do každého řádku.</li><li>**Stejné částky** – Částka je přidělena rovnoměrně pro každý řádek.</li><li>**Procento** – Částka je přidělena na základě procentuální hodnoty zadané pro každý řádek.</li><li>**Procento dokončení** – Pro každý řádek se vloží kumulativní hodnota dokončení.</li><p>**Variabilní množství** – pro každý řádek je vloženo množství přidělení.</li></ul><p>**Poznámka:** Pokud chcete vybrat **Procento dokončení**, data musí být ve vzestupném pořadí.</p> |
| **Vytvořit samostatné události pro každou jednotku** | |
| Popis | <p>Určete, zda chcete oddělit události na jednotku:</p><ul><li>**Ano** – Oddělte řádky událostí tak, aby na každé množství připadal jeden řádek.<p>Například existují tři řádky událostí a faktura má množství čtyři. V tomto případě má výsledný jízdní řád 12 řádků.</p></li><li>**Ne** – Neoddělujte řádky událostí.</li></ul> |
| Účet vypršení platnosti | <p>Vyberte účet, který se používá pro uznané řádky, jejichž platnost vypršela. Účet můžete vybrat po vytvoření plánu odkladu.</p><p>Pokud je pro událost nastaveno datum vypršení platnosti, během procesu rozpoznávání přejde částka uznání na účet pro ukončení platnosti namísto na účet pro uznání.</p> |
| **Plán – řádky na základě události** | |
| Popis | Popis události. |
| Koncové datum odkladu | <p>Vyberte koncové datum události.</p><p>**Poznámka:** Pokud vyberete datum ukončení, pole **Datum vypršení platnosti** je vymazáno. Nemůžete použít současně datum ukončení a datum vypršení platnosti.</p> |
| Datum vypršení platnosti | <p>Vyberte datum vypršení platnosti události.</p><p>**Poznámka:** Pokud vyberete datum ukončení, pole **Datum vypršení platnosti** je vymazáno. Nemůžete použít současně datum ukončení a datum vypršení platnosti.</p> |
| Množství | <p>Zadejte množství přidělení. Výchozí hodnota pro všechny řádky je **0** (nula). Pokud aktualizujete množství, celkové množství všech řádků musí být stejné nebo menší než množství zadané pro položku řádku v prodejní objednávce.</p><p>Toto pole je dostupné pouze v případě, že pole **Typ přidělení** je nastaveno na **Variabilní množství**.</p><p>Pokud se změní množství řádkové položky v prodejní objednávce tak, že je menší než původní množství, a vytvoří se faktura, vytvoří se méně řádků na základě událostí. Celkové přidělené množství nepřesahuje množství, které je uvedeno v původní prodejní objednávce nebo fakturačním plánu.</p> |
| Přidělená procenta | <p>Zadejte alokační procento. Pokud je pole **Typ přidělení** nastaveno na **Procento** nebo **Procento dokončení**, můžete ručně zadat procento. V opačném případě se automaticky počítá.</p><p>Pokud je pole **Typ přidělení** nastaveno na **Procento**, celkové procento se musí rovnat 100.</p> |
| Částka | <p>Zadejte částku přidělení. Pokud je pole **Typ přidělení** nastaveno na **Variabilní částka** nebo **Procento dokončení**, můžete ručně zadat částku.</p><p>Pokud je pole **Typ přidělení** nastaveno na **Procento dokončení** a zde zadáte částku, hodnota pole **Procento dokončení** se vypočítá automaticky.</p><p>Kvůli zaokrouhlování nemusí vypočítaná částka přesně odpovídat tomu, co je ručně zadáno. Pokud požadujete přesnou částku, nastavte pole **Typ přidělení** na **Variabilní částky**.</p> |
| Procento dokončení | <p>Zadejte procento dokončení. Hodnota musí být mezi 0 (nula) a 100.</p><p>Toto pole je dostupné pouze v případě, že pole **Typ přidělení** je nastaveno na **Procento dokončení**.</p> |
| Částka dokončení | <p>Vypočítaný součet pro všechny řádky v plánu odkladu.</p><p>Pokud je pole **Typ přidělení** nastaveno na **Procento dokončení**, můžete ručně zadat částku. V tomto případě se hodnota pole **Procento dokončení** vypočítá na základě částky, kterou zadáte.</p><p>Kvůli zaokrouhlování nemusí vypočítaná částka přesně odpovídat tomu, co je ručně zadáno.</p><p>Toto pole je dostupné pouze v případě, že pole **Typ přidělení** je nastaveno na **Procento dokončení**.</p> |
| Uznat při zaúčtování | <p>Zadejte, zda je řádek automaticky rozpoznán, jakmile je transakce zaúčtována:</p><ul><li>**Vybráno** - Zadejte, zda je řádek automaticky rozpoznán, jakmile je transakce zaúčtována.</li><li>**Vymazáno** - Řádek není rozpoznán, jakmile je transakce zaúčtována.</li></ul> |
| Účet pro uznání | <p>Zadejte rozpoznávací účet pro událost, pokud se účet liší od účtu, který se používá pro celý plán odkladu.</p><p>Toto pole můžete použít ve spojení s možností **Uznat při zaúčtování**.</p> |
