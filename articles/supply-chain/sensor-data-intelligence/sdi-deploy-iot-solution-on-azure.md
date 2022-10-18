---
title: Nasazení řešení IoT v Azure
description: Sensor Data Intelligence využívá data ze senzorů, které jsou připojeny k Microsoft Azure. Tento článek vysvětluje, jak nasadit řešení internetu věcí (IoT) ve vašem předplatném Azure.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5026f234f1b2f38e7041098421d0261fd468db96
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643706"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Nasazení řešení IoT v Azure

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensor Data Intelligence využívá data ze senzorů, které jsou připojeny k Microsoft Azure. Chcete-li umožnit Azure načítat data z vašich senzorů a sdílet je s Dynamics 365 Supply Chain Management, musíte na předplatné Azure nasadit řešení internetu věcí (IoT). Následující architektonický diagram poskytuje přehled řešení a jeho součástí.

![Architektonický diagram Sensor Data Intelligence.](media/sdi-architecture.png "Architektonický diagram Sensor Data Intelligence")

## <a name="video-instructions"></a>Video s pokyny

Následující video ukazuje, jak [zapnout funkci Sensor Data Intelligence](sdi-enable-feature.md) a nasadit požadované prostředky Azure. Další část tohoto článku poskytuje stejné pokyny v textovém formátu.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>Procedura

Postupujte podle následujících kroků k nasazení požadovaných prostředků na Azure.

1. Přihlaste se do prostředí Supply Chain Management jako správce.
1. Přejděte do nabídky **Správa systému \> Nastavení \> Sensor Data Intelligence \> Nasazení a připojení prostředků Azure** pro otevření průvodce nasazením.
1. Na stránce **Vítejte** si přečtěte informace a poté vyberte **Další**.
1. Na stránce **Nasazení ukázkového řešení IoT do Azure** si přečtěte informace a poté v části **Pokyny** vyberte **Nasadit**.
1. Otevře se nová karta prohlížeče a budete přesměrováni na portál Azure, kde můžete nasadit prostředky Azure. Pokud se zobrazí výzva, přihlaste se pomocí svých přihlašovacích údajů pro předplatné Azure.
1. Na stránce **Vlastní nasazení** v poli **Předplatné** vyberte své předplatné.
1. V části **Skupina prostředků** vyberte **Vytvořit nový** k vytvoření skupiny prostředků pro součásti Azure, které nasadíte.
1. V rozevíracím dialogovém okně, které se zobrazí, do pole **Název** zadejte název nové skupiny prostředků (např. *IoT-demo*). Pak vyberte **OK**.
1. Nastavte následující pole:

    - **Skupina prostředků** – Vyberte skupinu prostředků, kterou jste právě vytvořili.
    - **Region** – Vyberte oblast, ideálně oblast, kde je nasazeno vaše prostředí Supply Chain Management. Mějte na paměti, že oblasti Azure mají různé ceny. Odhadované náklady pro váš region můžete zobrazit pomocí [Cenové kalkulačky Sensor Data Intelligence](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **Adresa URL prostředí Supply Chain Management** – Zadejte adresu URL vašeho prostředí Supply Chain Management.
    - **Znovu použít stávající Azure IoT Hub** – Ponechte toto zaškrtávací políčko prázdné.

1. Vyberte **Další: Zkontrolovat + vytvořit**.
1. Na stránce **Vlastní nasazení** ověřte úspěšné ověření a vyberte **Ano**.
1. Stránka **Nasazování probíhá** sleduje průběh vašeho nasazení. Proces nasazení může trvat až 30 minut. Když stránka **Nasazování probíhá** ukazuje, že je nasazení dokončeno, vyberte odkaz pro název skupiny prostředků a otevřete stránku se seznamem prostředků, které jsou nasazeny ve skupině.
1. V seznamu zdrojů najděte záznam, kde je pole **Typ** nastaveno na *Spravovaná identita*. Ve sloupci **Název** vyberte název k otevření stránky s údaji o prostředku.
1. Zkopírujte hodnotu v poli **ID klienta** (například výběrem tlačítka **Zkopírovat do schránky**).
1. Vraťte se na kartu prohlížeče, kde běží Supply Chain Management, *ale nezavírejte kartu pro Azure Portal*. Stránka průvodce **Nasadit ukázkové řešení IoT do Azure** musí být stále otevřená. 
1. Zvolte **Další**.
1. Na stránce **Připojit prostředky Azure** do pole **ID klienta aplikace Azure AD** zadejte hodnotu **ID klienta**, kterou jste zkopírovali.
1. Vraťte se na kartu prohlížeče, kde je otevřený Azure Portal, *ale nezavírejte kartu pro Supply Chain Management*. Stránka s údaji prostředku musí zůstat otevřená.
1. Vyberte tlačítko **Zpět** prohlížeče pro návrat na seznam prostředků v nové skupině prostředků.
1. V seznamu prostředků najděte záznam, kde je pole **Typ** nastaveno na *Azure Cache for Redis*. Ve sloupci **Název** vyberte název k otevření stránky s údaji o prostředku.
1. V levém navigačním podokně nalevo vyberte položku **Přístupové klíče**.
1. Na stránce **Přístupové klíče** hodnotu zobrazenou pro **Primární připojovací řetězec (StackExchange.Redis)** (například výběrem tlačítka **Zkopírovat do schránky**).
1. Vraťte se zpět na kartu prohlížeče, kde běží Supply Chain Management. Stránka **Připojit prostředky Azure** musí být stále otevřená.
1. Do pole **Připojovací řetězec úložiště metriky Redis** vložte hodnotu **Primární připojovací řetězec (StackExchange.Redis)**, kterou jste zkopírovali.
1. Vyberte **Dokončit**.

Prostředky Azure pro Sensor Data Intelligence jsou nyní nasazeny ve vašem předplatném Azure.

> [!NOTE]
> Kdykoli můžete zobrazit nebo upravit informace o připojení uložené v Supply Chain Management otevřením stránky **Parametry Sensor Data Intelligence**. Další informace naleznete v tématu [Parametry Data Intelligence senzoru](sdi-parameters.md).
