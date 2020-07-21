# hello-world
Just another repository

This XML file does not appear to have any style information associated with it. The document tree is shown below.
<!-- Copyright 2014 Bluetooth SIG, Inc. All rights reserved. -->
<Service xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://schemas.bluetooth.org/Documents/service.xsd" type="org.bluetooth.service.bond_management" uuid="181E" name="Bond Management Service" last-modified="10-17-2014" approved="Yes">
<InformativeText>
<Abstract> This Specification proposes that this service will enable users to manage their bonds on devices with a limited user interface. </Abstract>
<Summary> This service defines how a peer Bluetooth device can manage the storage of bond information, especially the deletion of it, on the Bluetooth device supporting this service. </Summary>
</InformativeText>
<Dependencies>
<Dependency> This Service has no dependencies to other GATT-based services. </Dependency>
</Dependencies>
<GATTRequirements>
<Requirement subProcedure="Write Characteristic Values">Mandatory</Requirement>
<Requirement subProcedure="Write Long Characteristic Values">C1</Requirement>
<Requirement subProcedure="Reliable Writes">Optional</Requirement>
</GATTRequirements>
<Note> C1: Mandatory if operand longer than MTU is requested, else optional </Note>
<Transports>
<Classic>true</Classic>
<LowEnergy>true</LowEnergy>
<HighSpeed>true</HighSpeed>
</Transports>
<ErrorCodes>
<ErrorCode name="Op Code not supported" code="0x80" Description="Response if unsupported Op Code is received"/>
<ErrorCode name="Operation failed" code="0x81" Description="Response if unable to complete a procedure for any reason"/>
</ErrorCodes>
<Characteristics>
<Characteristic type="org.bluetooth.characteristic.bond_management_control_point" name="Bond Management Control Point">
<Requirement>Mandatory</Requirement>
<Properties>
<Read>Excluded</Read>
<Write>Mandatory</Write>
<WriteWithoutResponse>Excluded</WriteWithoutResponse>
<SignedWrite>Excluded</SignedWrite>
<ReliableWrite>Optional</ReliableWrite>
<Notify>Excluded</Notify>
<Indicate>Excluded</Indicate>
<WritableAuxiliaries>Excluded</WritableAuxiliaries>
<Broadcast>Excluded</Broadcast>
<ExtendedProperties>Excluded</ExtendedProperties>
</Properties>
<SecuritySettings>
<Security>Authentication</Security>
</SecuritySettings>
</Characteristic>
<Characteristic type="org.bluetooth.characteristic.bond_management_feature" name="Bond Management Feature">
<Requirement>Mandatory</Requirement>
<Properties>
<Read>Mandatory</Read>
<Write>Excluded</Write>
<WriteWithoutResponse>Excluded</WriteWithoutResponse>
<SignedWrite>Excluded</SignedWrite>
<ReliableWrite>Excluded</ReliableWrite>
<Notify>Excluded</Notify>
<Indicate>Excluded</Indicate>
<WritableAuxiliaries>Excluded</WritableAuxiliaries>
<Broadcast>Excluded</Broadcast>
<ExtendedProperties>Excluded</ExtendedProperties>
</Properties>
<SecuritySettings>
<Security>Authentication</Security>
</SecuritySettings>
</Characteristic>
</Characteristics>
</Service>
