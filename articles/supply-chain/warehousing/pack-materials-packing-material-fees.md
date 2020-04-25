---
title: Obalové materiály a poplatky
description: Toto téma obsahuje informace o poplatcích za obalový materiál, které jsou zaplaceny recyklačním společnostem v určitých intervalech.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1061f336701461df7a2cf78661788e4c6100c84d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215693"
---
# <a name="packing-materials-and-fees"></a>Obalové materiály a poplatky

[!include [banner](../includes/banner.md)]

Poplatky za balicí materiál se recyklační společnosti hradí v určitých intervalech. Platí se částka za hmotnostní jednotku za každý materiál, ze kterého se skládá jednotka balného. Ačkoli poplatky za balicí materiál jsou vypočítány a vykázány, nezaúčtují se žádné nikdy neúčtované transakce, protože poplatky se nepovažují za daně, které je třeba zaplatit úřadům.

Hmotnosti a poplatky za balicí materiály se počítají pro řádky prodejní objednávky i nákupní objednávky.

Pro položku, skupinu položek balení (skupinu balení) nebo pro všechny položky můžete definovat jednu nebo více jednotek balného. Jednotka balení obsahuje obalové materiály, jejich hmotnost a počet jednotek, které jsou obsaženy v jednotce balení. Kód obalového materiálu je přiřazen ke každému definovanému typu obalového materiálu. Na základě kódu obalového materiálu můžete stanovit cenu za určité období. Poplatku za obalový materiál je počítán na základě těchto informací.

> [!NOTE]
> I když vaše společnost neplatí poplatky za obalový materiál, lze funkci použít ke statistickým výpočtům hmotností obalového materiálu.

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a>Nastavení přidělení obalového materiálu

Než bude možné vypočítat hmotnosti balicího materiálu, poplatky za obalový materiál nebo obojí, je nutné tento výpočet zapnout a definovat, které materiály a poplatky se použijí pro položky.

1. Přejděte do nabídky **Řízení zásob \> Nastavení \> Parametry řízení zásob a skladu**.
1. Na kartě **Obecné** nastavte možnost **Vypočítat poplatky za obalový materiál** v části **Obalový materiál** na hodnotu **Ano**.
1. Přejděte na **Řízení zásob \> Nastavení \> Obalový materiál \> Skupiny balení** a vytvořte všechny skupiny balení, které používáte. Všechny položky v rámci skupiny balení budou používat stejné přidělení obalového materiálu. Pokud nepoužíváte skupiny balení, můžete tento krok přeskočit.

    > [!TIP]
    > Po vytvoření skupin balení můžete ke každému produktu přiřadit skupinu podle potřeby. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**, vyberte produkt a potom na pevné záložce **Spravovat sklad**, v poli **Skupina balení** vyberte příslušnou skupinu balení.

1. Přejděte na **Řízení zásob \> Nastavení \> Obalový materiál \> Kódy obalového materiálu**, defininujte jednotlivé typy obalového materiálu, který se používáte, a určete jednotky, v níž je obalový materiál spotřebován, při přípravě dodávek.
1. Přejděte na **Řízení zásob \> Nastavení \> Obalový materiál \> Poplatky za obalový materiál** a nastavte poplatek pro každý typ obalového materiálu, který jste právě definovali. Poplatky se počítají na základě ceny za jednotku, která je spotřebována.
1. Chcete-li k položkám přidělit balicí materiál , přejděte na **Řízení zásob \> Nastavneí \> Obalový materiál \> Přidělení obalového materiálu** a vytvořte přidělení. Můžete vytvořit tolik přidělení, kolik potřebujete. Můžete přidělit obalový materiál pro jednotlivé položky, skupiny položek (skupiny balení) nebo pro všechny položky v závislosti na tom, jak podrobné by vaše přidělení mělo být.

    Pro každé přidělení, které vytvoříte, postupujte takto.

    1. Na pevné záložce **Obecné** zadejte následující pole:

        - **Kód položky** – vyberte rozsah přidělení:

            - **Tabulka** – vytvoření přidělení pro jednu konkrétní položku.
            - **Skupina** – vytvoření přidělení pro všechny položky, které patří do skupiny balení definované na stránce **Skupiny balení**.
            - **Vše** – vytvoření přidělení pro všechny položky.

            > [!NOTE]
            > Obvykle by měla všechna vaše přidělení být na stejné úrovni (**tabulka**, **skupina** nebo **vše**). Pokud použijete více než jednu úroveň, bude pro každou položku použito nejkonkrétnější přidělení párování. (Úroveň **tabulka** má přednost před úrovní **skupina** a obě tyto úrovně mají přednost před úrovní **vše**.)

        - **Vztah položky** – pokud provádíte přidělení pro jednu položku, vyberte danou položku. Pokud provádíte přidelení pro skupinu položek, vyberte skupinu balení. Pokud provádíte přidělení pro všechny položky, ponechejte toto pole prázdné.
        - **Konfigurace**, **Velikost**, **Barva** a **Styl** – zadejte hodnoty pro tyto dimenze podle potřeby, chcete-li dále definovat položku, pro kterou provádíte přidělení.
        - **Jednotka balení** – vyberte jednotku, v níž je položka zabalena při použití obalového materiálu. Tato jednotka se může lišit od jednotky, ve které je položka nakoupena a uložena.
        - **Koeficient jednotky balení** – zadejte koeficient převodu, který se použije pro převod skladové jednotky na jednotku balení. (Při převodu se použije receptura *Jednotky balení* = *jednotky položky* x *faktor jednotky balení*.)

    1. Na pevné záložce **Obalový materiál** přidejte řádek pro každý kus obalového materiálu, který je požadován pro aktuální přidělení. Na každém řádku určete typ materiálu (jak je definován na stránce **Kódy obalového materiálu**) a množství, které je spotřebováno pro každou expedovanou jednotku aktuální položky.

## <a name="packing-units-on-sales-order-lines"></a>Jednotky balení na řádcích prodejní objednávky

Po [zapnutí výpočtu poplatků za obalový materiál a nastavení přidělení](#allocations) systém ověří, zda jsou jednotky balení zadány pro každou položku, která je přidána do prodejní objednávky. Systém poté vypočítá všechny požadované poplatky. Při přidání položky do prodejní objednávky dojde k jednomu z následujících kroků:

- **Pokud pro položku platí přidělení balení:** Systém aktualizuje řádek prodejní objednávky o příslušnou jednotku balení a množství jednotky balení. (Množství jednotky balného je vypočítáno s použitím receptury *množství jednotky balení* = *objednané množství* ÷ *počet položek vybrané jednotky balného*.)
- **Pokud pro položku neplatí přidělení balení:** Jednotku balení a množství jednotky balení na řádku prodejní objednávky můžete zadat ručně.

Při zaúčtování řádku prodejní objednávky lze rovněž změnit jednotku balení a množství jednotky balení. To má význam v případě, kdy je řádek prodejní objednávky částečně doručen nebo fakturován.

Při fakturaci prodejní objednávky systém vytvoří transakce obalového materiálu. Transakce obalového materiálu obsahuje hmotnost obalového materiálu pro řádky prodeje. Transakce lze upravit po jejich fakturaci. Poté můžete vytvořit nové transakce.

## <a name="packing-units-on-purchase-order-lines"></a>Jednotky balení na řádcích nákupní objednávky

Systém nevytvoří transakce obalového materiálu pro řádky nákupní objednávky. Místo toho na stránce **Transakce obalového materiálu** můžete ručně vytvořit transakce pro fakturované řádky nákupní objednávky.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Nastavení licenčních čísel pro odběratele, kterým jsou účtovány poplatky za obalový materiál

Chcete-li, aby prodejní objednávky pro konkrétního odběratele zahrnovaly náklady na obalový materiál, které jsou použity pro každou objednávku, postupujte podle následujících kroků.

1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. Vyberte odběratele, kterému by měly být zaúčtovány poplatky za obalový materiál.
1. Na pevné záložce **Faktury a dodávky** zadejte následující pole:

    - V sekci **DPH** v poli **Číslo licence balného** zadejte číslo licence společnosti.
    - V sekci **Poplatek za obalový materiál** v poli **Číslo licence** zadejte číslo licence společnosti.

Když nyní vytvoříte a fakturujete prodejní objednávku, která obsahuje jednu nebo více položek, které používají obalové materiály, faktura zobrazí poplatky za obalový materiál.

Pro odběratele, kteří by neměli platit za obalové materiály, postupujte podle stejných kroků, ale vymažte pole **Číslo licence balného** a **Číslo licence**. Faktury pro odběratele, kteří nemají platit za obalový materiál, obsahují hmotnost obalových materiálů, ale neobsahují poplatky.

Chcete-li vygenerovat sestavu zobrazující všechny poplatky za obalový materiál, které bude vaše společnost dlužit za určité období, přejděte na **Řízení zásob \> Dotazy a sestavy \> Sestavy obalového materiálu \> Výpočet poplatku za obalový materiál**, zadejte rozsah dat a poté vyberte **OK**.

## <a name="print-packing-material-weights-on-invoices"></a>Tisk hmotnosti obalových materiálů na fakturách

Na faktuře můžete vytisknout hmotnost obalových materiálů a informovat o tom, kdo platí související poplatky. Hmotnosti se sčítají pro jednotlivé kódy obalu.

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
1. Na kartě **Aktualizace** na pevné záložce **Faktura** nastavte volbu **Tisk hmotnosti obalového materiálu** na hodnotu **Ano**.
