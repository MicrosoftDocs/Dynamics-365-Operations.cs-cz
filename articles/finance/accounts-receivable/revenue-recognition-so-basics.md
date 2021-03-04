---
title: Uznání výnosů na prodejních objednávkách
description: Toto téma popisuje základní funkci pro uznání výnosů na prodejních objednávkách a fakturách. Uznání výnosů je k dispozici na prodejních objednávkách a příslušné faktuře, která je vytvořena z prodejní objednávky.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6212ecbf1883405d7ca8cb1dba752b778e4d901c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995535"
---
# <a name="revenue-recognition-on-sales-orders"></a>Uznání výnosů na prodejních objednávkách

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Funkci uznání výnosů nelze zapnout prostřednictvím správy funkcí. V současné době ji aktivujete pomocí konfiguračních klíčů.

Toto téma popisuje základní funkci pro uznání výnosů na prodejních objednávkách a fakturách. Uznání výnosů je k dispozici na prodejní objednávce a příslušné faktuře, která je vytvořena z prodejní objednávky. Prodejní objednávku lze rovněž vytvořit prostřednictvím projektů určených materiálem a časem.

> [!NOTE]
> Na ilustracích v tomto tématu byly sloupce skryty nebo přidány do mřížky, aby se lépe zobrazily koncepty. Stránky a data na obrázcích se proto mohou lišit od toho, co vidíte v produktu.

## <a name="enter-a-sales-order"></a>Zadání prodejní objednávky

Následující prodejní objednávka je zadána a zahrnuje tři položky, které jsou nastaveny pro uznání výnosů.

[![Zadání prodejní objednávky](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Pro uznání výnosů existují dva koncepty:

- **Určení výnosové ceny.** Výnosová cena se vypočítává na základě nastavení uvolněných produktů. Výnosová cena se nikdy nezobrazuje zákazníkovi, ale používá se pouze pro účetnictví faktury prodejní objednávky. Řádky prodejní objednávky a dokumenty, které se vytisknou jako součást prodeje, nadále zobrazují jednotkovou/ceníkovou cenu.
- **Určení, kdy má dojít k uznání výnosů.** K určení toho, kdy mají být výnosy uznány, se používá plán výnosů.

    V tomto příkladu je první položka S0001 přiřazena k plánu výnosů **1O** (jednorázově). Tento řádek představuje scénář milníkového typu, kdy výnosy budou uznány, jakmile dojde v budoucnu k instalaci. Výnosy budou proto odloženy do dokončení instalace.

    Druhá položka, S0008, je položkou služby, která je nastavena jako položka podpory po uzavření smlouvy. Trvalé inženýrské služby jsou zákazníkovi poskytovány po dobu 12 měsíců. Proto je ve výchozím nastavení produktu přiřazen plán výnosů **12M**. Protože je tato položka položkou podpory po uzavření smlouvy, je třeba definovat počáteční a koncová data smlouvy. Ve výchozím nastavení jsou počáteční a koncová data smlouvy uvedena na kartě Podrobnosti položky - Nastavení. V plánu výnosů je nastavení pro **12M** definováno tak, aby smluvní podmínky byly automaticky vyplněny, jak je znázorněno na následujícím obrázku.

    [![Plány výnosů](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Třetí položka, S0012, je hardware a ve výchozím nastavení není přiřazen žádný plán výnosů. Výnosy za hardware jsou uznány, jakmile je položka vyfakturována.

## <a name="confirm-the-sales-order"></a>Potvrzení prodejní objednávky

Chcete-li zobrazit další podrobnosti o výnosové ceně a plánu příjmů, použijte tlačítka ve skupině **Uznání výnosů** na kartě **Správa** v podokně akcí prodejní objednávky. Protože v tomto okamžiku není prodejní objednávka potvrzena, tlačítka, která se používají pro uznání výnosů, nejsou k dispozici. Tato tlačítka se stávají dostupnými nebo nedostupnými, jak prodejní objednávka postupuje ve fázích vedoucích k plnění.

[![Záhlaví prodejní objednávky](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

První tři tlačítka poskytují podrobnosti o výnosové ceně pro položky v nastavení prodejní objednávky pro uznání výnosů.

- **Přidělení výnosové ceny** – Toto tlačítko bude k dispozici po potvrzení prodejní objednávky nebo zaúčtování faktury. Potvrzení prodejní objednávky i účtování faktur počítají výnosy k uznání ceny, která bude uznána nebo odložena na účetní položce. V závislosti na nastavení se vypočtená výnosová cena může lišit od jednotkové ceny, která se zobrazuje zákazníkovi.
- **Opětovné přidělení ceny k novým řádkům objednávky** – Toto tlačítko bude k dispozici po potvrzení prodejní objednávky nebo zaúčtování faktury. Proces opětovného přidělení se používá k přepočtu výnosů, které musí být uznány po přidání nového řádku do aktuální prodejní objednávky po její fakturaci, nebo do nové prodejní objednávky. V obou scénářích způsobí přidání nové položky změnu smlouvy. Proto musí být výnosová cena opětovně přidělena.
- **Aktualizace přidělení výnosové ceny** – Toto tlačítko bude k dispozici po potvrzení prodejní objednávky, ale přestane být dostupné po vyfakturování prodejní objednávky. Tato aktualizace slouží k opětovnému spuštění přidělení výnosové ceny bez nutnosti potvrzení prodejní objednávky. Po fakturaci prodejní objednávky nelze výnosovou cenu přepočítat.

Poslední dvě tlačítka poskytují podrobnosti o plánu výnosů pro ty položky v prodejní objednávce, které mají plán výnosů.

- **Očekávaný plán uznání výnosů** – Toto tlačítko bude k dispozici po potvrzení prodejní objednávky, ale přestane být dostupné po vyfakturování prodejní objednávky. Otevře se stránka, která ukazuje očekávaný plán výnosů. Konečný plán se může změnit, protože očekávaný plán používá požadované datum expedice, zatímco konečný plán používá skutečné datum expedice.
- **Plán uznání výnosů** – Toto tlačítko bude k dispozici po vyfakturování prodejní objednávky. Konečný plán uznání výnosů se nevytvoří, když dojde k potvrzení nebo je vytvořen dodací list. Vytvoří se pouze tehdy, když je prodejní objednávka vyfakturována.

V následujícím příkladu došlo k přidělení výnosové ceny, když byla potvrzena prodejní objednávka. Pamatujte, že ačkoli jsou výnosové ceny přiděleny různě, celková částka v poli **Výnosy k uznání** se musí stále rovnat součtu řádků prodejní objednávky, které jsou fakturovány zákazníkovi. Například součet řádků prodejní objednávky bez daně je 1 499 USD. Proto součet hodnot **Výnosy k uznání** musí být též 1 499 USD.

[![Přidělení výnosové ceny](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Vytvoří se také očekávaný plán uznání výnosů. Plán výnosů používá hodnotu **Výnosy k uznání** jako částku k odložení. Položka S0001 odkládá 321,21 USD namísto 300 USD a položka S0008 odkládá 160,61 USD namísto 100 USD. Položka S0012 se nezobrazuje v očekávaném plánu, protože výnosy nejsou odloženy. Když dojde k zaúčtování, položka S0012 zaúčtuje 1 017,18 USD přímo na účet hlavní knihy výnosů.

[![Očekávaný plán uznání výnosů](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Vytvoření dodacího listu

Dále lze pro prodejní objednávku vytvořit dodací list. Po zaúčtování dodacího listu nejsou uznány žádné výnosy. Pokud nebyla prodejní objednávka potvrzena, zaúčtování dodacího listu nespouští výpočet výnosové ceny. Nespouští také vytvoření očekávaného nebo konečného plánu uznání výnosů. Pokud je skupina modelu položek nastavena tak, aby odkládala výnosy na dodacím listu, bude pokračovat v účtování pomocí hlavní knihy účetního profilu, nikoli nových účtů odložených výnosů, které se používají při zaúčtování faktur.

## <a name="create-the-invoice"></a>Vytvoření faktury

Posledním krokem je fakturace prodejní objednávky. Pokud se podíváte na doklad faktury, zjistíte, že výnosy pro položky S0001 a S0008 byly odloženy (321,21 + 160,61 = 481,82 USD) a zbývající částka pro položku S0012 byla zaúčtována do výnosů (1 017,18). Tyto hodnoty dají dohromady 1 499 USD, což odpovídá součtu řádků prodejní objednávky.

[![Transakce dokladu](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Po vytvoření faktury budou k dispozici tlačítka pro uznání výnosů **Přidělení výnosové ceny**, **Opětovné přidělení ceny k novým řádkům objednávky** a **Plán uznání výnosů**, ale tlačítka **Aktualizace přidělení výnosové ceny** a **Očekávaný plán uznání výnosů** nebudou dostupná.

[![Dostupnost tlačítek uznání výnosů](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

Tlačítko **Přidělení výnosové ceny** je stále k dispozici, abyste mohli zobrazit výpočet výnosové ceny. Pokud se po potvrzení objednávky na prodejní objednávce nic nezmění, zaúčtování faktury nezmění vypočítanou částku v poli **Výnosy k uznání**.

Očekávaný plán uznání výnosů je odstraněn a nahrazen konečným plánem uznání výnosů. Podrobnosti plánu výnosů jsou udržovány pro každý řádek prodejní objednávky a používají se k uvolnění odložených výnosů do skutečných výnosů, jakmile jsou splněny smluvní závazky.

[![Konečný plán uznání výnosů](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)
