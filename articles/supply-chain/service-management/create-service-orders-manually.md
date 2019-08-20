---
title: Ruční vytvoření servisních objednávek
description: Servisní zakázky můžete vytvářet ručně pomocí servisní smlouvy nebo pomocí formuláře **Servisní zakázky**.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbe1ccc90b215c35f44835b1307977c18927bd7e
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743296"
---
# <a name="create-service-orders-manually"></a>Ruční vytvoření servisních objednávek    

[!include [banner](../includes/banner.md)]


Servisní zakázky můžete vytvářet ručně pomocí servisní smlouvy nebo pomocí formuláře **Servisní zakázky**. Servisní zakázku můžete také vytvořit z projektu.

> [!TIP]
> <P>Automatizované procesy slouží k vytváření servisních zakázek. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Ruční vytvoření servisní zakázky ze servisní smlouvy

1.  Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.

2.  Vyberte servisní smlouvu nebo vytvořte novou servisní smlouvu.

3.  Klikněte na kartu **Dodávka** a ve skupině **Vytvořit**klikněte na **Plánované servisní zakázky** k otevření formuláře **Vytvořit servisní zakázky**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Ruční vytvoření servisní zakázky ve formuláři Servisní zakázky

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  Stisknutím kláves Ctrl+N vytvořte novou servisní zakázku.

3.  Vytvořte řádky servisní zakázky pro servisní smlouvu.

> [!NOTE]
> <P>Jestliže je zaškrtnuto políčko <STRONG>Povolit bez servisní smlouvy</STRONG> ve formuláři <STRONG>Parametry servisní smlouvy</STRONG>, můžete transakce z řádků servisní zakázky účtovat bez připojení servisní zakázky k servisní smlouvě. Jestliže políčko není zaškrtnuto, je před zaúčtováním řádků servisní zakázky nutné připojit ručně vytvořenou servisní zakázku k projektu.</P>

## <a name="create-a-service-order-from-a-project"></a>Vytvoření servisní zakázky z projektu

1.  Klikněte na **Řízení a účetnictví projektů** \> **Společné** \> **Projekty** \> **Všechny projekty**.

2.  Ve formuláři **Projekty** v **podokně akcí** klikněte na kartu **Správa** \> klikněte na **Servis** \> **Servisní příkazy**.

3.  Postupujte podle pokynů pro ruční vytvoření servisní zakázky ve formuláři **Servisní zakázky**. V poli **ID projektu** se zobrazuje reference na projekt.

> [!NOTE]
> <P>Jestliže je zaškrtnuto políčko <STRONG>Povolit bez servisní smlouvy</STRONG> ve formuláři <STRONG>Parametry servisní smlouvy</STRONG>, můžete transakce z řádků servisní zakázky účtovat bez připojení servisní zakázky k servisní smlouvě. Jestliže políčko není zaškrtnuto, je před zaúčtováním řádků servisní zakázky nutné připojit ručně vytvořenou servisní zakázku k projektu.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Vytvoření servisních zakázek z formuláře Prodejní objednávka

Servisní zakázku lze vytvořit z formuláře **Prodejní objednávky** pomocí průvodce **Vytvoření nové servisní zakázky na základě prodejní objednávky**.

1.  Klikněte na **Prodej a marketing** \> **Společné** \> **Prodejní objednávky** \> **Všechny prodejní objednávky**.

2.  Otevřete příslušnou prodejní objednávku.

3.  Na kartě **Prodejní objednávka** spusťte kliknutím na **Servisní zakázka** průvodce **Vytvoření nové servisní zakázky na základě prodejní objednávky**.

4.  Klepněte na tlačítko **Další \>** a poté proveďte následující kroky na stránce **Vybrat smlouvu pro servisní zakázku**:
    
      - V poli **Servisní smlouva** vyberte servisní smlouvu, ke které by nová servisní zakázka měla být přidružena.
    
      - (Volitelné): Použijte pole **ID projektu** pro přidružení servisní zakázky ke konkrétnímu projektu.

5.  Klepněte na tlačítko **Další \>** a poté proveďte následující kroky na stránce **Vytvořit servisní zakázku**:
    
      - Do pole **Upřednostňovaný čas služby** zadejte datum a čas zahájení volání servisu.
    
      - V případě potřeby text v poli **Popis**. Ve výchozím nastavení obsahuje toto pole popis, který je popisem servisní smlouvy vybrané na předchozí stránce.
    
      - V poli **Zodpovědná osoba** vyberte ID zaměstnance, který je odpovědný za smlouvu, a pokud znáte ID technika preferovaného odběratelem pro volání servisu, zadejte je.
    
      - V poli **ID kontaktu** vyberte osobu ze společnosti odběratele, která by měla být v souvislosti s touto servisní zakázkou kontaktována.

6.  Klikněte na **Další \>** a potom na **Dokončit**.


## <a name="see-also"></a>Viz také

[Servisní zakázky](service-orders.md)

[Automatické vytvoření servisních zakázek](create-service-orders-automatically.md)

[Vytvoření servisních zakázek (formulář třídy)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 

