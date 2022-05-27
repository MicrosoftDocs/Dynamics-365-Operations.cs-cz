---
title: Plány odkladu při odkladech výnosů a výdajů
description: Toto téma popisuje plány odkladu při odkladech výnosů a výdajů.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9135ac733496a0c5d79669c35972c273c209f81d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685970"
---
# <a name="deferral-schedules"></a>Plány odkladu

Plány odkladů se vytvářejí po zaúčtování transakce.

Můžete použít stránku **Všechny plány odkladů** nebo **Aktivní plány odkladů**, kde najdete podrobnosti o plánu odkladu. Zobrazené informace závisí na typu plánu odkladu (přímý nebo na základě událostí) a typu transakce. Zahrnuje řádky plánu odkladu a celkové částky pro plán odkladu. Pomocí stránky můžete upravit plán odkladu.

## <a name="recognize-revenue"></a>Uznání výnosů

> [!NOTE]
> - Chcete-li zaúčtovat výnosy pro jeden plán odkladu, začněte krokem 1.
> - Chcete-li uznat výnosy pro více plánů, začněte krokem 2.

1. Na stránce **Všechny plány odkladů** v mřížce **Řádky plánů** vyberte řádky, které chcete uznat, a poté vyberte **Uznat**.
2. Na stránce **Zpracování uznání** nastavte pole **Akce uznání** na **Vytvořit deník uznání**.
3. V poli **Datum přerušení** vyberte datum přerušení. Zpracování bude zahrnovat pouze řádky, jejichž datum ukončení je dřívější nebo stejné jako vybrané datum uzávěrky.
4. Vyberte **Filtr** a přidejte datové filtry tak, aby seznam zobrazoval pouze požadovaný rozsah záznamů.
5. Vyberte **Zobrazit náhled** pro zobrazení řádků.
6. V seznamu řádků vyberte řádky, které nechcete zpracovat, a poté vyberte **Odstranit**.
7. Vyberte, zda chcete shrnout záznam deníku rozpoznávání.
8. V sekci **Datum transakce** můžete přepsat datum transakce konkrétním datem zpracování transakce. Pro uzavřená období lze zadat datum transakce.
9. Chcete-li provést zpracování jako součást dávky, vyberte **Dávka**. V dialogovém okně **Dávkové zpracování** nastavte parametry pro dávku a poté vyberte **OK**, chcete-li se vrátit na stránku **Zpracování rozpoznávání**. Zaúčtování výnosů bude zpracováno později, až bude dávka zpracována.
10. Vyberte možnost **Proces**. Pokud jste transakci nepřidali do dávky, všechny řádky jsou okamžitě zpracovány. V opačném případě budou řádky zpracovány při zpracování dávky.

## <a name="modify-a-schedule"></a>Úprava plánu

Při úpravách plánu odkladu postupujte takto.

1. Na stránce **Všechny plány odkladů** vyberte plán odkladu a poté vyberte **Účetnictví \> Upravit plán**.
2. Na stránce **Upravit plán** upravte možnosti, které chcete změnit. V závislosti na plánu odkladu nebudete moci upravit všechny možnosti.
3. Vyberte **Náhled**, chcete-li zkontrolovat změny v plánu odkladu.
4. Vyberte **OK**.

### <a name="straight-line-deferral-schedules"></a>Plány odložení rovných řádků

Pokud plán odkladu nemá žádné rozpoznané nebo externě zaúčtované řádky, můžete upravit celý plán odkladu, včetně data zahájení.

Pokud má plán odkladu nějaké rozpoznané nebo externě zaúčtované řádky a upravíte plán odložení, výsledné chování plánu odložení závisí na datu přepočtu a datu ukončení odložení uznaných řádků. Ve výchozím nastavení určuje datum ukončení odkladu první období, které nebylo rozpoznáno.

Chcete-li použít datum rozpoznání, vyberte jednu z následujících hodnot v poli **Začátek plánu**: 
- **Zachycení** – Částka po přepočtu všech rozpoznaných řádků.
- **Storno** – Všechny řádky po datu přepočtu jsou stornovány pomocí zadaného názvu deníku a data účtování. Částka po datu přepočtu se pak přepočítá.

Pokud je použita šablona, vynechaná období jsou ignorována a šablona se používá pouze k výpočtu data ukončení.

### <a name="event-based-deferral-schedules"></a>Plány odkladů založené na událostech

U plánu odložení na základě události můžete upravit všechny nerozpoznané linky.

Pokud plán odkladu nemá žádné rozpoznané nebo externě zaúčtované řádky, nemůžete upravit šablonu a typ přidělení pro plán odkladu. Když upravíte existující plán odložení, nemůžete změnit hodnotu pole **Vytvořte samostatné události pro jednotku**.

Pokud je řádek rozpoznán nebo externě zaúčtován, je vybráno zašrtávací políčko **Uznáno**.

## <a name="modify-a-deferral-or-recognition-account"></a>Upravte účet pro odložení nebo uznání

Chcete-li upravit účet odložení nebo uznání pro plán odložení, postupujte takto.

1. Na stránce **Všechny plány odkladů** vyberte plán odkladu a poté vyberte **Účetnictví \> Upravit účet**.
2. Na stránce **Upravit účet** vyberte účet, který chcete změnit (odložený, krátkodobý nebo uznání).
3. V poli **Nový účet** vyberte nový účet.
4. Vyberte, zda změny na účtu vytvářejí účetní zápisy oprav.
5. Pokud nastavíte možnost na **Ano** v předchozím kroku, vyberte název deníku v poli **Název deníku** a zadejte datum transakce v poli **Datum transakce**.
6. Vyberte **OK**.

## <a name="put-a-deferral-schedule-on-hold"></a>Blokace plánu odkladu

Při blokaci plánu odkladu postupujte takto.

1. Na stránce **Všechny plány odkladů** vyberte plán odkladu a poté vyberte **Blokování \> Blokovat**.
2. Na stránce **Blokovat** vyberte, zda chcete převést zůstatek z odloženého účtu nebo pozdrženého účtu.
3. Pokud jste vybrali převod zůstatku, vyberte název deníku v poli **Název deníku**, vyberte účet blokace v poli **Blokovaný účet** a zadejte datum transakce v poli **Datum transakce**.
4. Vyberte **OK**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Odstraňte blokaci z plánu odkladu

Chcete-li odebrat plán odkladu z blokace, postupujte takto.

1. V seznamu **Všechny plány odkladů** vyberte plán odkladu a poté vyberte **Blokování \> Odstranit blokaci**.
2. V poli **Název deníku** vyberte název deníku.
3. V poli **Datum transkace** zadejte datum transakce.
4. Vyberte **OK**.

## <a name="cancel-unrecognized-amounts"></a>Zrušit neuznané částky

> [!NOTE]
> Všechny řádky, které již byly rozpoznány nebo externě zaúčtovány, jsou z tohoto procesu vyloučeny.

Při stornu nerozpoznaných částek z plánu odkladu postupujte takto.

1. Na stránce **Všechny plány odkladů** vyberte plán odkladu a poté vyberte **Storno \> Nerozpoznané částky**.
2. Na stránce **Zrušit nerozpoznanou částku** vyberte, zda chcete vytvořit záznamy o zrušení.
3. Pokud jste vybrali vytvoření storna položek, vyberte název deníku v poli **Název deníku**, vyberte účet storna v poli **Účet storna** a zadejte datum transakce v poli **Datum transakce**.
4. Vyberte **OK**.

## <a name="cancel-a-completed-schedule"></a>Zrušení dokončeného plánu

Použijte stránku **Všechny plány odkladů**, chcete-li stornovat jakékoli uznané nebo externě zaúčtované částky a zrušit plán odkladu, aby se zabránilo dalšímu zaúčtování.

Při stornu célého plánu odkladu postupujte takto.

1. Na stránce **Všechny plány odkladů** vyberte plán odkladu a poté vyberte **Storno \> Celý plán**.
2. Na stránce **Zrušit celý plán** vyberte, zda chcete vytvořit záznamy o zrušení.
3. Pokud jste vybrali vytvoření storna položek, vyberte název deníku v poli **Název deníku**, vyberte účet v poli **Účet storna** a zadejte datum transakce v poli **Datum transakce**.
4. Vyberte **OK**.

## <a name="reverse-transactions"></a>Stornovat transakce

> [!NOTE]
> - Chcete-li stornovat uznání výnosu pro jeden plán odkladu, začněte krokem 1.
> - Chcete-li stornovat uznání výnosu pro více plánů odkladu, začněte krokem 2.

1. Na stránce **Všechny plány odkladů** v mřížce **Řádky plánů** vyberte řádky, u kterých chcete zrušit uznání, a poté vyberte **Storno**.
2. Na stránce **Zpracování uznání** nastavte pole **Akce uznání** na **Storno deník uznání**.
3. V poli **Datum přerušení** vyberte datum přerušení. Zpracování bude zahrnovat pouze řádky, jejichž datum ukončení je dřívější nebo stejné jako zadané datum uzávěrky.
4. Vyberte **Filtr** a přidejte datové filtry tak, aby seznam zobrazoval pouze požadovaný rozsah záznamů.
5. Vyberte **Zobrazit náhled** pro zobrazení řádků.
6. V seznamu řádků vyberte řádky, které nechcete zpracovat, a poté vyberte **Odstranit**.
7. Pole **Název** a **Popis** se automaticky aktualizují výchozím názvem a popisem deníku. Hodnoty můžete podle potřeby měnit. Můžete také vybrat, zda chcete shrnout záznam deníku rozpoznávání.
8. V sekci **Datum transakce** můžete přepsat datum transakce konkrétním datem zpracování transakce. Pro uzavřená období lze zadat datum transakce.
9. Chcete-li provést zpracování jako součást dávky, vyberte **Dávka**. V dialogovém okně **Dávkové zpracování** nastavte parametry pro dávku a poté vyberte **OK**, chcete-li se vrátit na stránku **Zpracování rozpoznávání**. Storno uznání výnosů bude zpracováno později, až bude dávka zpracována.
10. Vyberte **OK**. Pokud jste transakci nepřidali do dávky, všechny řádky jsou okamžitě zpracovány. V opačném případě budou řádky zpracovány při zpracování dávky.

## <a name="apply-or-unapply-a-credit-note"></a>Použijte nebo zrušte použití dobropisu

Chcete-li použít dobropis vytvoříte takto.

> [!NOTE]
> Když vytvoříte dobropis ze stránky **Odložení transakce prodejní objednávky** a nastavíte možnost **Upravit stávající plán** na **Ano**, dobropis se automaticky použije do plánu při zaúčtování dobropisu.

1. Na stránce **Všechny plány odkladů** vyberte plán odkladu.
2. V seznamu **Úpravy úvěrů** vyberte řádek a poté vyberte **Použít**.
3. Na stránce **Použít dobropis (odklady)** zadejte datum přepočtu v poli **Datum přepočtu** a koncové datum v poli **Datum ukončení**.
4. V seznamu **Hlaviček** vyberte **Prodejní objednávku**, která má dobropisy.
5. V seznamu **Řádky** vyberte řádek.
6. Vyberte **OK**.
7. Vyberte **Ano**.

> [!NOTE]
> Chcete-li použít dobropis na několik jednotlivých položek z různých faktur, musíte tyto kroky zopakovat.

Chcete-li zrušit použití dobropisu, postupujte takto.

1. Na stránce **Všechny plány odkladů** vyberte plán odkladu.
2. V seznamu **Úpravy úvěrů** vyberte fakturu a poté vyberte **Zrušit použití**.
3. Vyberte **Ano**.

## <a name="fields"></a>Pole

Stránka **Všechny plány odkladů** obsahuje následující pole.

| Pole | Popis |
|--------|-------------|
| **Záhlaví** | |
| **Plán** | |
| Typ přidělení | Typ přidělení pro odklady založené na událostech: **Procento** nebo **Částka**. |
| Datum reklasifikace | <p>Poslední datum, kdy byla zpracována krátkodobá reklasifikace pro plán odkladu. Toto datum se aktualizuje pokaždé, když se **Krátkodobá reklasifikace události** použije pro plán odkladu.</p>Toto pole je dostupné pouze v případě, že je použita metoda klouzavého období nebo metoda krátkodobého odložení s pevným rokem. |
| **Účet** | |
| Účet pro odklad | Účet, který se používá pro částku odkladu. |
| Účet pro uznání | Účet, který se používá pro částku uznání. |
| Typ uznání | Typ uznání. |
| Typ distribuce | Typ distribuce. |
| **Transakce** | |
| Zdroj vytvoření | Zdroj, ze kterého byla transakce vytvořena. |
| Typ transakce | Typ transakce. |
| Prodejní objednávka | Číslo prodejní objednávky. |
| Faktura | Číslo faktury. |
| Položka | Číslo položky. |
| **Plán fakturace** | |
| Číslo plánu fakturace | Číslo položky příslušného plánu fakturace. |
| Stav řádku fakturace | Stav položky příslušného řádku plánu fakturace. |
| Externí odkazy | Informace o externích referencích z plánu fakturace: **Externí** a **Číslo řádku**. |
| Součty | <p>Celkové částky pro plán odkladu:</p><ul><li>**Dlouhodobý** – Součet dlouhodobě odložených částek. Tato hodnota je dostupná pouze tehdy, když je pole **Metoda krátkodobého odkladu** je nastaveno na **Žádný** na stránce **Parametry odkladu výnosů a nákladů** nebo je krátkodobá částka větší než 0 (nula).</li><li>**Krátkodobý** – Součet krátkodobě odložených částek. Tato hodnota je dostupná pouze tehdy, když je pole **Metoda krátkodobého odkladu** je nastaveno na **Žádný** na stránce **Parametry odkladu výnosů a nákladů** nebo je krátkodobá částka větší než 0 (nula).</li><li>**Neuznané** - Součet neuznaných částek pro všechny řádky.</li><li>**Neúplné** - Součet externě zaúčtovaných částek pro všechny řádky.</li><li>**Uznané** - Součet uznaných částek pro všechny řádky.</li><li>**Externě zaúčtované a uznané** – Součet externě zaúčtovaných a uznaných částek za všechny řádky.</li><li>**Celková částka** - součet částek všech řádků.</li></ul> |
| **Řádky plánu** | |
| Řádek | Číselná řada řádků. |
| Počáteční datum odkladu | Počáteční datum plánu odkladu. |
| Koncové datum odkladu | Koncové datum plánu odkladu. |
| Částka | Částka odkladu. |
| Externě zaúčtované | Hodnota, která označuje, zda byl řádek externě zaúčtován. |
| Uznáno | Hodnota, která označuje, zda byl řádek uznán. |
| Číslo dávky deníku | Číslo dávky, ve které byla částka uznána. |
| Popis události | Popis události. Toto pole je dostupné pouze pro plány odkladu založené na událostech. |
| **Úpravy kreditu** | |
| Faktura | <p>Číslo faktury.</p><p>Hodnota označuje fakturu za úpravu dobropisu, která již byla uplatněna v plánu odkladu.</p> |
| Použitá částka | Částka úpravy úvěru, která již byla použita v plánu odkladu. |
| Datum použití | Datum, kdy byla provedena úprava úvěru. |
| **Úprava** | Hodnoty úprav se zobrazí pouze v případě, že byl pro plán odkladu zpracován dobropis. Pokud nebyl zpracován žádný dobropis, jsou tyto hodnoty skryté. |
| Částka úpravy | Celková opravná částka vypočtená jako *Původní částka* – *Částka plánu*. |
| Datum původního ukončení | Původní koncové datum plánu odkladu. |
| Původní částka plánu | Celkový původní plán odkladu. |
