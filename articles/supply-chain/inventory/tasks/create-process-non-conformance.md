---
title: Vytvoření a zpracování neshod
description: Toto téma popisuje provádění správy neshody na základě existující objednávky kvality.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956199"
---
# <a name="create-and-process-nonconformances"></a>Vytvoření a zpracování neshod

[!include [banner](../../includes/banner.md)]

Toto téma popisuje provádění správy neshody na základě existující objednávky kvality. Řízení neshod obvykle provádí úředník pro kvalitu. Předpokladem je, že musíte mít k dispozici objednávku kvality. (Informace o tom, jak vytvořit objednávku kvality, viz [Kontrola kvality zboží](inspect-quality-goods.md) .)

Než může uživatel zpracovat schválení neshody, musí mu být přiřazen pracovník v poli **Osoba** na stránce **Uživatelé**. Než bude uživatel moci používat poznámky k dokumentu, musí být navíc možnost **Povolit zpracování dokumentů** nastavena na *Ano* v uživatelských možnostech.

## <a name="create-a-nonconformance"></a>Vytvoření neshody

Pokud chcete vytvořit neshodu, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V podokně Akce zvolte **Nový**.
1. V dialogovém okně **Vytvoření neshody** v poli **Typ problému** vyberte typ problému, který byl nalezen během procesu kontroly.
1. Vyberte **OK**.

## <a name="approve-or-reject-a-nonconformance"></a>Schválení nebo zamítnutí neshody

Chcete-li schválit nebo zamítnout neshodu, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V seznamu vyberte neshodu, kterou chcete aktualizovat.

    > [!NOTE]
    > Opravu můžete přidat pouze ke neshodám, které jsou schváleny.

1. V podokně akcí vyberte **Funkce \> Schválit neshodu** ke schválení neshody nebo **Funkce \> Odmítnout neshodu** k jejímu odmítnutí. Schválené neshody můžete přidružit k [souvisejícím operacím](../quality-operations.md). Tímto způsobem můžete zaznamenat práci, která se provádí jako součást zpracování neshod a zpracování oprav.
1. Budete vyzvání k potvrzení výběru. Pokračujte výběrem tlačítka **Ano**.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Přidání operací a dalších údajů k neshodám

Po vytvoření neshody můžete začít přidávat související operace a určit další informace o těchto operacích. Související operace můžete přidat pouze ke neshodám, které jsou schváleny.

Kromě základních informací můžete k operaci přidat následující údaje:

- **Položky** – Můžete vytvořit seznam položek, které jsou spotřebovány k provedení opravy. Položky mohou být například výrobky, které jsou nutné k opravě zařízení, nebo přísady, které jsou nutné k přepracování hotového výrobku.
- **Poplatky za kvalitu** – Můžete vytvořit seznam poplatků, které jsou účtovány externím zdrojům.
- **Rozvrh hodin** – Můžete vytvořit protokol času, který každý pracovník stráví operací.

Zbývající nastavení jsou volitelná. Náklady na každou položku, poplatky za kvalitu a časový rozvrh jsou sečteny a zobrazeny na operaci. Nelze přímo upravit pole **Náklady** operace.

### <a name="create-an-operation-for-a-nonconformance"></a>Vytvoření operace pro neshodu

Pokud chcete vytvořit operaci pro neshodu, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V seznamu vyberte neshodu, kterou chcete aktualizovat.

    > [!NOTE]
    > Operace můžete přidat nebo aktualizovat pouze u neshod, které jsou schváleny.

1. V podokně Akce vyberte možnost **Související operace**.
1. Na stránce **Související operace** v podokně Akce vyberte **Nový** a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Operace** – Vyberte kód operace, která bude provedena pro nesoulad.
    - **Důvod** – Zadejte podrobný popis, který vysvětluje, proč je operace požadována.
    - **Prodejní objednávka** – Pokud vybraný kód operace souvisí s typem prodejní objednávky, vyberte prodejní objednávku, se kterou operaci propojujete.
    - **Nákupní objednávka** – Pokud vybraný kód operace souvisí s typem nákupní objednávky, vyberte nákupní objednávku, se kterou operaci propojujete.

1. Zavřete stránky.

### <a name="add-items-to-an-operation"></a>Přidání položek do operace

Chcete-li přidat položky do operace, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V seznamu vyberte neshodu, kterou chcete aktualizovat.

    > [!NOTE]
    > Operace můžete přidat nebo aktualizovat pouze u neshod, které jsou schváleny.

1. V podokně Akce vyberte možnost **Související operace**.
1. Na stránce **Související operace** vyberte operaci, do které chcete přidat položky.
1. V podokně akcí zvolte **Položky**.
1. Na stránce **Související operace** v podokně Akce vyberte **Nový** a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Číslo položky** – Vyberte produkt, který bude spotřebován jako součást vybrané operace.
    - **Množství** – Zadejte počet položek, které budou spotřebovány.

    > [!NOTE]
    > Náklady na položku můžete zobrazit v poli **Náklady** na kartě **Obecné** záložka. Cena, která se zde zobrazuje, pochází z nákladů, které jsou nastaveny na stránce **Vydaný produkt**. Náklady nelze aktualizovat přímo na stránce **Související položka operace**. Cena všech položek, které jsou přidány na stránku **Související položky operace**, se automaticky přidá do pole **Náklady** na stránce **Související operace**.

1. Opakujte předchozí krok pro každou další položku, kterou musíte přidat.
1. Zavřete stránky.

### <a name="add-quality-charges-to-an-operation"></a>Přidání poplatků za kvalitu k operaci

Chcete-li přidat poplatky za kvalitu k operaci, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V seznamu vyberte neshodu, kterou chcete aktualizovat.

    > [!NOTE]
    > Operace můžete přidat nebo aktualizovat pouze u neshod, které jsou schváleny.

1. V podokně Akce vyberte možnost **Související operace**.
1. Na stránce **Související operace** vyberte operaci, do které chcete přidat poplatky za kvalitu.
1. V podokně Akce vyberte možnost **Poplatky za kvalitu**.
1. Na stránce **Související poplatky operace** v podokně Akce vyberte **Nový** a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Kód poplatků** – Vyberte poplatek za kvalitu, který chcete přidat.
    - **Popis** - Zadejte podrobný popis typu nákladu.
    - **Hodnota poplatků** – Zadejte částku poplatku.

1. Opakujte předchozí krok pro každý poplatek, který musíte přidat.
1. Zavřete stránky.

> [!NOTE]
> Částka v poli **Hodnota poplatků** je automaticky sečtena pro všechny poplatky za kvalitu a přidána k jakýmkoli dalším částkám v poli **Náklady** na stránce **Související operace**.

### <a name="create-a-timesheet-on-an-operation"></a>Vytvoření časového rozvrhu operace

Chcete-li časový rozvrh k operaci, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V seznamu vyberte neshodu, kterou chcete aktualizovat.

    > [!NOTE]
    > Operace můžete přidat nebo aktualizovat pouze u neshod, které jsou schváleny.

1. V podokně Akce vyberte možnost **Související operace**.
1. Na stránce **Související operace** vyberte operaci, do které chcete přidat časový rozvrh.
1. V podokně akcí zvolte **Časový rozvrh**.
1. Na stránce **Související časové rozvrhy operace** v podokně Akce vyberte **Nový** a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Datum** – Uveďte datum, kdy byla práce dokončena. Ve výchozím nastavení je toto pole nastaveno na aktuální datum.
    - **Pracovník** – Vyberte pracovníka, který práci provedl. Ve výchozím nastavení je toto pole nastaveno na pracovníka, který je přiřazen aktuálnímu uživateli.
    - **Provozní doba** – Zadejte počet hodin, které byly odpracovány na vybrané operaci.
    - **Fakturováno** – Toto políčko zaškrtněte, pokud byl čas účtován zákazníkovi nebo prodejci na faktuře.

    > [!NOTE]
    > Náklady si můžete prohlédnout v poli **Náklady** na kartě **Obecné**. Cena se vypočítá pomocí sazby, kterou definujete na stránce **Parametry správy zásob**.

1. Opakujte předchozí krok pro každý řádek časového rozvrhu, který musíte přidat.
1. Zavřete stránky.

> [!NOTE]
> Částka v poli **Náklady** je sečtena pro všechny řádky časového rozvrhu a přičtena k jakýmkoli dalším částkám v poli **Náklady** na stránce **Související operace**.

## <a name="add-a-correction-to-a-nonconformance"></a>Přidání opravy k neshodě

Chcete-li přidat opravu k neshodě, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V seznamu vyberte neshodu, kterou chcete aktualizovat.

    > [!NOTE]
    > Opravu můžete přidat pouze ke neshodám, které jsou schváleny.

1. V podokně akcí zvolte **Opravy**.
1. Na stránce **Opravy** v podokně Akce vyberte **Nový** pro přidání řádku do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Diagnostika** – Vyberte typ diagnostiky, který určuje typ opravy, kterou vytváříte.
    - **Pracovník** – Vyberte osobu, která za opravu nese odpovědnost.
    - **Priorita opravy** – Vyberte možnost a určete, jak by měla být korekce upřednostněna (*Nízký*, *Normální* nebo *Vysoký*).
    - **Požadované datum** – Zadejte datum, kdy bylo požadováno nápravné opatření.
    - **Plánované datum** – Zadejte datum, kdy se očekává dokončení opravy.
    - **Krátkodobé řešení** – Zaškrtněte toto políčko, pokud nápravná akce opraví nesoulad pouze na krátkou dobu.

1. Zavřete stránky.

## <a name="mark-a-correction-as-completed"></a>Označení opravy jako dokončené

Chcete-li označit opravu neshody jako dokončenou, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V seznamu vyberte neshodu, kterou chcete aktualizovat.

    > [!NOTE]
    > Opravu můžete přidat pouze ke neshodám, které jsou schváleny.

1. V podokně akcí zvolte **Opravy**.
1. Na stránce **Opravy** v mřížce vyberte opravu, kterou chcete označit jako dokončenou.
1. V podokně akcí vyberte možnost **Označit jako dokončenou**.
1. Budete vyzvání k potvrzení výběru. Pokračujte volbou tlačítka **OK**. Pole **Datum a čas dokončení** pole je nastaveno na aktuální datum a čas a je zaškrtnuto políčko **Dokončeno**.
1. Zavřete stránku.

## <a name="reopen-a-completed-correction"></a>Opětovné otevření dokončené opravy

Chcete-li otevřít dokončenou opravu, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.
1. V seznamu vyberte neshodu, kterou chcete aktualizovat.
1. V podokně akcí zvolte **Opravy**.
1. Na stránce **Opravy** v mřížce vyberte opravu, kterou chcete znovu otevřít.
1. V podokně akcí zvolte **Znovu otevřít**.
1. Budete vyzvání k potvrzení výběru. Pokračujte volbou tlačítka **OK**. Hodnota je vymazána z pole **Datum a čas dokončení** a políčko **Dokončeno** není zaškrtnuto.
1. Zavřete stránku.

Nyní můžete provést další úpravy nebo aktualizace opravy. Po dokončení můžete opravu znovu označit jako dokončenou.

## <a name="close-a-nonconformance"></a>Zavření neshody

Pokud chcete zavřít neshodu, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.
1. Vyberte objednávku kvality v mřížce.
1. V podokně akcí zvolte **Dotazy \> Neshody**.
1. Na stránce **Neshody** vyberte cílovou neshodu v mřížce.
1. V podokně Akce zvolte **Funkce \> Zavřít neshodu**.
1. Budete vyzvání k potvrzení výběru. Pokračujte výběrem tlačítka **Ano**.
1. Zavřete stránky.

## <a name="additional-resources"></a>Další prostředky

- [Přehled správy kvality](../quality-management-processes.md)
- [Povolit správu kvality a neshod](../enable-quality-management.md)
- [Zaměstnanci odpovědní za schvalování neshod](../quality-responsible-workers.md)
- [Karanténní zóny pro neshody](../quality-quarantine-zones.md)
- [Diagnostické typy pro neshody](../quality-diagnostic-types.md)
- [Kódy kvality pro náklady](../quality-charges.md)
- [Operace pro neshody](../quality-operations.md)
- [Správa kvality pro procesy skladu](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
