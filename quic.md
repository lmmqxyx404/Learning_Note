2.3. Stream Prioritization

Stream multiplexing can have a significant effect on application performance if resources allocated to streams are correctly prioritized.

QUIC does not provide a mechanism for exchanging prioritization information. Instead, it relies on receiving priority information from the application.

3. Stream States

Note: In some cases, a single event or action can cause a transition through multiple states. For instance, sending STREAM with a FIN bit set can cause two state transitions for a sending stream: from the "Ready" state to the "Send" state, and from the "Send" state to the "Data Sent" state.

# frame
## There are multiple different frame types.
a packet contains many frames. and at least one frame.

# packet