# [Apache Arrow](https://arrow.apache.org/)

Arrow defines two types of binary formats for serializing record batches (`RecordBatch`):
- **Streaming** format: for sending an arbitrary length sequence of record batches.
  - The format must be processed from start to end
  - API: `RecordBatchStreamWriter`
  - aka. [IPC Streaming Format](https://arrow.apache.org/docs/format/Columnar.html#ipc-streaming-format)
- **File** or Random Access format: for serializing a fixed number of record batches.
  - Supports random access
  - very useful when used with memory maps
  - `RecordBatchFileReader` = `RecordBatchStreamReader` + a `seek` method for random access
  - > The `RecordBatchFileWriter` has the same API as `RecordBatchStreamWriter`
  - aka. [IPC File Format](https://arrow.apache.org/docs/format/Columnar.html#ipc-file-format)
  - has a footer containing: 1. **a redundant copy of the schema** 2. memory **offsets and sizes** for each of the data blocks in the file

Arrow NativeFile: The base class for all Arrow streams.

## Ref
[data-integration: stream or batch](https://github.com/davidkhala/data-integration/wiki#stream-vs-batch)
